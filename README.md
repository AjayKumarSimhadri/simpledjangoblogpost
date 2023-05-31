# simpledjangoblogpost
---
## Django Simple Blog Project
---
This is a simple blog project created using Django.

In the context of a Django blog project, a "blog post" refers to an individual article or entry that is published on the blog. It typically includes a title, content, and additional metadata such as the publication date, author, and tags/categories. Blog posts are the main content units that users can create, read, edit, and delete within the blog application. They are displayed on the blog's webpages and can be organized and categorized based on various criteria, such as date, category, or tag. Blog posts allow users to share information, ideas, opinions, or stories with the readership of the blog.

## Getting Started

Follow the steps below to set up your development environment and start using the project.

### Prerequisites

- Python
- Django

### Environment Setup

1. Open the command prompt or terminal.
2. Navigate to the project directory using the `cd` command. For example:
   ```
   cd project-name
   ```
3. Create a virtual environment for Django:
   ```
   python -m venv myenv
   ```
4. Activate the virtual environment:
   - For Windows:
     ```
     myenv\Scripts\activate
     ```
   - For macOS/Linux:
     ```
     source myenv/bin/activate
     ```
5. Once the virtual environment is activated, you can install Django by running the following command:
   ```
   pip install django
   ```
6. After Django is installed, you can proceed with other project-specific dependencies or installations.

### Create a Superuser

To access the Django admin area, you need to create a superuser. Run the following command and provide the requested information:
```
python manage.py createsuperuser
```
Follow the prompts to enter a username, email (optional), and password for the superuser.

### Database Migrations

To apply database migrations, run the following commands:
```
python manage.py makemigrations
python manage.py migrate
```

### Running the Project

To run the project on the local development server, execute the following command:
```
python manage.py runserver
```
You can now access the blog project by visiting `http://localhost:8000` in your web browser.

## Project Structure

The project structure is as follows:

- `blog/` - The main Django application folder.
- `templates/` - Contains the HTML templates used for rendering the webpages.
- `static/` - Stores static files like CSS, JavaScript, and images.
- `media/` - Location for user-uploaded media files.
- `manage.py` - Django's command-line utility for various management tasks.
- `requirements.txt` - List of project dependencies.

## Development Steps

1. Set up the development environment by creating a Django project and adding a blog app to it. Create a Django superuser for the admin area and configure the database model for the blog posts.
2. Use Django's class-based views to create webpages out of the blog posts. Look at the ListView and DetailView and see how to create views and URLs for each of them.
3. Add a new field to the database to record the HTML title tag for each unique blog post. Create a migration for the new model and apply it to the database.
4. Use the Django admin area to add blog posts and create actual webpages where you can write blog posts.
5. Create a backend form using a forms.py file and add widgets to the form to import Bootstrap form-control CSS.
6. Create a new form that allows editing specific fields.
7. Implement functionality to delete blog posts in Django. Make a slight modification that differs from other views and use reverse_lazy redirection after deleting a post.
8. Handle old posts that don't have a date listed by making appropriate provisions during migrations.
9. Utilize Django's built-in user authentication system to allow people to register, log in, and log out.
10. Implement functionality to show different content based on user login status. If a user is logged in, they should be able to log out, edit posts, delete posts, and add new posts. If a user isn't logged in, they shouldn't be able to add, edit, or delete posts.
11. Use the `safe` filter in Django to escape HTML characters in blog posts.
12. Add a 'category' designation for each blog post. Start by adding a category field to the Post database model. Then, create a Category model to add, edit, or remove categories from the blog. Modify the forms.py file to designate a category for each new blog post.
13. Switch to function-based views to build category pages and pass the browser request through to the view.
14. Implement slug URLs for category pages using the Django `|slugify` filter and the Python `.replace()` function.
15. Use the Bootstrap Navbar code to create a dropdown menu with links to each of the category pages. Also, create a webpage with links to all the category pages.
16. Restrict editing or deleting a blog post to only the person who created it.
17. Restrict the add_post page to only allow logged-in users to make posts in their own name, not another user.
18. Implement a Many-to-Many database association to keep track of whether or not a logged-in user has liked a blog post. Create a blog like button.
19. Add an "unlike" button for users to remove their like from a blog post.
20. Modify the registration form to ask for first name, last name, and email address in addition to username and password.
21. Use the django-ckeditor package to stylize blog posts, add images, and links. Install it using `pip install django-ckeditor` and make the necessary tweaks to the models.py file, then create and apply the migration.
22. Implement article snippets to describe each blog post on the homepage. Use the first 20 characters of the blog post itself for the homepage snippet. With the rich text editor, this can be achieved easily.
23. Create a profile page where users can edit their profiles. Style it using Bootstrap.
24. Use Django admin functionality to allow users to change their password. Build a custom page that allows users to change their password without relying on the Django admin page.
25. Set up the ability to upload a header image for each blog post. Add a field to the database model, make changes to the settings.py file, and update the urls.py file accordingly.
26. Add a box below each blog post that shows the author's profile picture, links to their social media, and their author bio.
27. Create a dropdown link in the navbar with links to the profile page, user edit page, and profile page edit.
28. Set up the user profile page.
29. Implement comments by creating a Comment model in the models.py file and associating it with the Post model using a foreign key.
30. Use the Django admin area to post a comment on a blog post.

---

Please let <a href = "mailto: mail4ajay786@gmail.com">me</a> know if there's anything else I can help you with!
