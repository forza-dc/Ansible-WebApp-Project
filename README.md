# Ansible Web App Deployment Project

This Ansible project automates the deployment and configuration of a multi-tier web application. The web application consists of a frontend, backend, and a database. Additionally, the project includes roles for securing the servers and setting up monitoring.

## Project Structure

![File Hierarchy](<Ansible Web App File Hierarchy.png>)



## Project Overview

- **Common Role (`roles/common`):**
  - Updates the system packages.
  - Installs common utilities and dependencies.

- **Frontend Role (`roles/frontend`):**
  - Installs and configures Nginx for serving the frontend application.

- **Backend Role (`roles/backend`):**
  - Installs and configures Node.js and Express for the backend application.

- **Database Role (`roles/database`):**
  - Installs and configures PostgreSQL as the database server.

- **Security Role (`roles/security`):**
  - Configures firewall rules.
  - Applies security best practices.

- **Monitoring Role (`roles/monitoring`):**
  - Sets up Prometheus and Grafana for monitoring.

## Getting Started

Follow these steps to deploy the web application:

1. **Inventory Configuration:**
   - Update inventory files in `inventories/production` and `inventories/staging` with your server details.

2. **Variable Configuration:**
   - Update the variables in the role `group_vars` files to match your application requirements.

3. **Run the Playbook:**
   - Deploy to production:
     ```bash
     ansible-playbook -i inventories/production site.yml
     ```
   - Deploy to staging:
     ```bash
     ansible-playbook -i inventories/staging site.yml
     ```

4. **Customization:**
   - Modify YAML files based on your specific needs.
   - Expand the project as needed.

Feel free to customize and extend this project to fit your requirements. If you encounter any issues or have questions, refer to Ansible documentation or seek assistance from the community.
