---
title: Azure Active Directory Conditional Access FAQ | Microsoft Docs
description: 'Frequently asked questions about conditional access '
services: active-directory
documentationcenter: ''
author: MarkusVi
manager: femila

ms.assetid: 14f7fc83-f4bb-41bf-b6f1-a9bb97717c34
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 04/11/2017
ms.author: markvi

---
# Azure Active Directory Conditional Access FAQ

## Which applications work with conditional access policies?

**A:** Please see [Applications and browsers that use conditional access rules in Azure Active Directory](active-directory-conditional-access-supported-apps.md).

---

## Are conditional access policies enforced for B2B collaboration and guest users?
**A:** Policies are enforced for B2B collaboration users. However, in some cases, a user might not be able to satisfy the policy requirement if, for example, an organization does not support multi-factor authentication. 
The policy is currently not enforced for SharePoint guest users. The guest relationship is maintained within SharePoint. Guest users accounts are not subject to access polices at the authentication server. Guest access can be managed at SharePoint.

---

## Does a SharePoint Online policy also apply to OneDrive for Business?
**A:** Yes.

---

## Why can’t I set a policy on client apps, like Word or Outlook?
**A:** A conditional access policy sets requirements for accessing a service and is enforced when authentication happens to that service. The policy is not set directly on a client application; instead, it is applied when it calls into a service. For example, a policy set on SharePoint applies to clients calling SharePoint and a policy set on Exchange applies to Outlook.

--- 

## Does a conditional access policy apply to service accounts?
**A:** Conditional access policies apply to all user accounts. This includes user accounts used as service accounts. In many cases, a service account that runs unattended is not able to satisfy a policy. This is, for example the case, when MFA is required. In these cases, services accounts can be excluded from a policy, using conditional access policy management settings. Learn more about applying a policy to users here.

---

## Are Graph APIs available to configure configure conditional access policies?
**A:** not yet. 

---