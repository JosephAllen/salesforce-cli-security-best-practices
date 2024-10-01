# Salesforce CLI Security Best Practices

Welcome to the SFDX CLI Security Best Practices wiki!

## Mitigating Session Hijacking

> Session Hijacking is a customer-focused attack where attackers try to steal information from using a client’s access to a web application. In our case, this application is Salesforce. When a client successfully authenticates with Salesforce, they receive a session token. The attacker tries to hijack the client’s session by obtaining their session token.
>
> _from: [help.salesforce.com](https://help.salesforce.com/s/articleView?id=sf.real_time_em_threat_session.htm&type=5)_

## Outline

### Permission Sets

- Create a `Salesforce CLI` perm set for the app
  - Assign Users to the permission Set

### Connected Apps
- Install the app
- Click `Edit Policies`
- `Permitted users` = `Admin approved users are pre-authorized`
- Session Policies: High Assurance session required
  - Raise the session level to high assurance
- Add the `Salesforce CLI` permission set to the App

### Setup: Session Settings

- `Lock sessions to the IP address from which they originated`
