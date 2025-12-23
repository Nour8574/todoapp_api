# Todo App (Application de Gestion de Tâches)

## 1. Présentation générale
Le projet **Todo App** est une application web permettant de gérer les tâches quotidiennes. 
Le projet est développé avec **Laravel 12** et une architecture **API RESTful**.

## 2. Fonctionnalités principales
- **Liste des tâches** : consulter toutes les tâches.
- **Ajout d’une tâche** : créer une nouvelle tâche avec un titre et une description.
- **Modification d’une tâche** : mettre à jour le titre, la description ou l'état d'une tâche.
- **Suppression d’une tâche** : supprimer une tâche existante.
- **Sécurité et validation** : protection via middleware et validation des requêtes.

## 3. Architecture du projet
- **Model** : `Todo` avec attributs `id`, `title`, `description`, `is_completed`, `created_at`, `updated_at`.
- **Controller** : `TodoController` gère toutes les opérations CRUD.
- **Routes API** : définies dans `routes/api.php`.
- **Base de données** : SQLite pour le développement local.

### Exemple de routes
```php
Route::get('/todos', [TodoController::class, 'index']);
Route::post('/todos', [TodoController::class, 'store']);
Route::get('/todos/{id}', [TodoController::class, 'show']);
Route::put('/todos/{id}', [TodoController::class, 'update']);
Route::delete('/todos/{id}', [TodoController::class, 'destroy']);
4. Configuration et dépendances
Laravel 12
SQLite
Composer
Git/GitHub
5. Utilisation du projet
Cloner le projet :
git clone https://github.com/Nour8574/todoapp_api.git
cd todoapp_api
*/Installer les dépendances :
composer install
*/Configurer l’environnement :
Copier .env.example en .env.
*/Vérifier la configuration SQLite.
*/Créer la base de données et les tables :
php artisan migrate
*/Lancer le serveur Laravel :
php artisan serve
*/Tester l’API via Postman ou navigateur :
GET    /api/todos
POST   /api/todos
PUT    /api/todos/{id}
DELETE /api/todos/{id}
6. Conclusion
Ce projet est un exemple complet d’une application CRUD avec API RESTful, démontrant :
Gestion des routes et contrôleurs,
Configuration base SQLite,
Versionning via GitHub.