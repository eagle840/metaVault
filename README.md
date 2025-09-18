# metaVault
Store secrets with a web frontend


### 🔐 **Architecture Overview**

#### 1. **Secrets Storage: Azure Key Vault**
- **Pros**:
  - Secure, encrypted storage for secrets, keys, and certificates.
  - Role-based access control (RBAC) and audit logging.
  - Native integration with Azure services and SDKs.

#### 2. **Metadata Storage: Azure Blob Storage**
- Use this to store:
  - Descriptions
  - Notes
  - Documentation or related files (e.g., JSON/YAML configs)
- You could store metadata as JSON blobs, or even use **Azure Table Storage** or **Cosmos DB** if you want structured querying.

#### 3. **Frontend: React**
- Great choice for a lightweight, responsive UI.
- You can use:
  - **MSAL.js** for Azure AD authentication.
  - **Azure SDK for JavaScript** to interact with Key Vault and Blob Storage.
  - A simple table/grid UI to list secrets, show metadata, and allow editing.

#### 4. **Backend (Optional)**
- If you want to abstract access or enforce business logic, consider a **Node.js or .NET API** layer.
- This can also help with caching, logging, and permission enforcement.

---

### 🧠 Additional Suggestions

- **Tagging in Key Vault**: You can use tags to store small metadata (e.g., owner, environment, purpose).
- **Audit Logs**: Enable diagnostic settings to log access to Key Vault for compliance.
- **Versioning**: Key Vault supports versioning of secrets—useful for rollback and auditing.


