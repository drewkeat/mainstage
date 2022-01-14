# Planning Notes

Started by creating two git repos (api/client)
Cleaned up boilerplate and set initial packages/gems

### Functionality
- Login
- Create a Production
  - Title
  - Venue
  - Description
  - Roles
  - Dates
    - Auditions
    - Rehearsals
    - Performances
  - Image
Community Openings
  - Audition/Apply
User Roles
  - Notes/Notifications
* Manage Productions
  - Edit Production Details
  - Review Audition/Interview

---
### Pages
- **Landing (Login)**
  - *Landing page with sign-in form and sign-up button*
  - PATH(S):
    1. GET: "/"
    2. POST: "/sessions
  - CONTROLLER:
    - sessions#create

- **Sign Up**
  - *Sign-up form with required user attributes*
  - PATH(S):
    1. GET: "/signup"
    2. POST: "/users"
  - CONTROLLER:
    - users#create

- **User Profile**
  - *Profile page, displays messages, productions and roles w/ links to:*
    - *My Productions*
    - *Community Callboard*
    - *Edit Profile*
  - PATH(S):
    1. GET: "/users/:id"
  - CONTROLLER:
    - users#show
  
- **Edit Profile**
  - *Displays a form to update user attributes and delete account*
  -  PATH(S):
     1. GET: "/users/:id/edit"
     2. PATCH: "/users/:id" 
     3. DELETE: "/users/:id"
  - CONTROLLER:
    - users#update
    - users#destroy

- **Community Callboard**
  - *Displays upcoming productions*
  - PATH(S):
    1. GET: "/productions
  - CONTROLLER:
    - productions#index

- **Production**
  - *Displays details regarding the production*
  - PATH(S):
    1. GET: "/productions/:id"
  - CONTROLLER:
    - productions#show

- **Register for Audition/Interview**
  - *Registration form for production audition or interview*
  - PATH(S):
    1. GET: "/productions/:id/registrations/new"
    2. POST: "/productions/:id/registrations"
  - CONTROLLER:
    - productions/registrations#create

- **My Productions**
  - *Display list of user-related productions*
  - PATH(S):
    - 1. GET: "/users/:id/productions
  - CONTROLLER:
    - productions#index

- **User Production**
  - *Displays Production Callboard with rehearsals, notes, messages, etc.*
  - PATH(S):
    1. GET: "/users/:id/productions/:id
  - CONTROLLER:
    - productions#show

- **Manage Production**
  - *Displays options associated with production management*
  - PATH(S):
    1. GET: "admin/productions/:id"
  - CONTROLLER:
    - admin/productions#show
  
- **Edit Production**
  - *Displays a form to edit production attributes*
  - PATH(S):
    1. GET: "/admin/productions/:id/edit
    2. PATCH: "/admin/productions/:id
  - CONTROLLER:
    - admin/productions#update
    - admin/productions#destroy
  
- **Auditions/Interviews**
  - *Description*
  - PATH(S):
    1. GET: 
  - CONTROLLER:
    - controller
  
- **Message Company**
  - *Description*
  - PATH(S):
    1. GET: 
  - CONTROLLER:
    - controller
  
- **PAGE**
  - *Description*
  - PATH(S):
    1. GET: 
  - CONTROLLER:
    - controller

### Routes
- / 
  - (root)
- /signup
  - (users#new)
- /users/:id
  - (user#show)
- /productions
  - (productions#index)
- /productions/:id
  - (productions#show)
- /new-production
  - (new)
- /user/productions/
  - (user/productions#index)
- /manage-production
  - (user/productions/production#edit)

### Models
- User
- Production 
- Audition
- Interview
- Reviewable
- Review