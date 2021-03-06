---
title: Understand Azure Digital Twins security best practices | Microsoft Docs
description: Azure Digital Twins security best practices
author: kingdomofends
manager: alinast
ms.service: digital-twins
services: digital-twins
ms.topic: conceptual
ms.date: 10/25/2018
ms.author: adgera
---

# Security best practices

Azure Digital Twins security enables precise access to specific resources and actions in your IoT graph. It does so through granular role and permission management called role-based access control.

Azure Digital Twins also uses other security features that are present on Azure IoT, which includes Azure Active Directory (Azure AD). For that reason, configuring your Azure Digital Twins app involves using many of the same [Azure IoT security practices](https://docs.microsoft.com/azure/iot-fundamentals/iot-security-best-practices?context=azure/iot-hub/) currently recommended.

This article summarizes key best practices to follow.

> [!IMPORTANT]
> To ensure maximal security for your IoT space, review additional security resources. Make sure to include your device vendors.

## IoT security best practices

Some key practices to safely secure your IoT devices include:

> [!div class="checklist"]
> * Secure each device that's connected to your IoT space in a tamper-proof way.
> * Limit the role of each device, sensor, and person within your IoT space. If compromised, the effect is minimized.
> * Consider the potential use of device IP address filtering and port restriction.
> * Limit I/O and device bandwidth to improve performance. Rate-limiting can improve security by preventing denial-of-service attacks.
> * Keep device firmware up to date.

Some key practices to safely secure an IoT space include:

> [!div class="checklist"]
> * Encrypt saved, stored, or persistent data.
> * Require passwords or keys to be periodically changed or refreshed.
> * Carefully restrict access and permissions by role. See the section "Role-based access control best practices."
> * Use powerful encryption. Require long passwords, and use secure protocols and two-factor authentication.

Monitor IoT resources to watch for outliers, threats, or resource parameters that fall outside the range of usual operation. Use Azure Analytics to manage the monitoring.

> [!NOTE]
> For more information on event processing and monitoring, see [Route events and messages with Azure Digital Twins](./concepts-events-routing.md).

## Azure Active Directory best practices

Azure Digital Twins uses Azure AD to authenticate users and protect applications. Azure AD supports authentication for a variety of modern architectures. They're all based on industry-standard protocols such as OAuth 2.0 or OpenID Connect. A few key practices to secure your IoT space for Azure AD include:

> [!div class="checklist"]
> * Store Azure AD app secrets and keys in a secure location, such as [Azure Key Vault](https://azure.microsoft.com/services/key-vault/).
> * Use a certificate issued by a trusted [certificate authority](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-certificate-based-authentication-get-started) rather than app secrets to authenticate.
> * Limit OAuth 2.0 scope of access for a token.
> * Verify the length of time a token is valid and whether a token remains valid.
> * Set appropriate lengths of time that tokens are valid for.
> * Refresh expired tokens.

## Role-based access control best practices

[!INCLUDE [digital-twins-rbac-best-practices](../../includes/digital-twins-rbac-best-practices.md)]

## Next steps

To learn more about Azure IoT best practices, read [IoT security best practices](https://docs.microsoft.com/azure/iot-fundamentals/iot-security-best-practices?context=azure/iot-hub/).

To learn about role-based access control, read [Role-based access control](./security-role-based-access-control.md).

To learn about authentication, read [Authenticate with APIs](./security-authenticating-apis.md).
