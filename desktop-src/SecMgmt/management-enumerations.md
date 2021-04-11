---
description: Listet die Enumerationen auf, die von den LSA-Richtlinien Verwaltungsfunktionen verwendet werden.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Sicherheitsverwaltungs-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216193"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="4261b-103">Sicherheitsverwaltungs-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4261b-103">Security Management Enumerations</span></span>

<span data-ttu-id="4261b-104">Die Sicherheitsverwaltungs-Enumerationen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4261b-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="4261b-105">LSA-Richtlinien Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4261b-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="4261b-106">Sicherere Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4261b-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="4261b-107">LSA-Richtlinien Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4261b-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="4261b-108">Die folgenden Enumerationstypen werden von den LSA-Richtlinien Verwaltungsfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4261b-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="4261b-109">Enumeration</span><span class="sxs-lookup"><span data-stu-id="4261b-109">Enumeration</span></span>                                                                               | <span data-ttu-id="4261b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4261b-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4261b-111">**Richtlinien Überwachungs- \_ \_ \_ Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="4261b-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="4261b-112">Definiert die Arten von Ereignissen, die das System überwachen kann.</span><span class="sxs-lookup"><span data-stu-id="4261b-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="4261b-113">**Richtlinien \_ Informations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="4261b-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="4261b-114">Definiert die Typen von Informationen, die für ein [**Richtlinien**](policy-object.md) Objekt festgelegt oder abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="4261b-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="4261b-115">**LSA-Richtlinien- \_ \_ Server \_ Rolle**</span><span class="sxs-lookup"><span data-stu-id="4261b-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="4261b-116">Geben Sie die Rolle eines LSA-Servers an.</span><span class="sxs-lookup"><span data-stu-id="4261b-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="4261b-117">**Richtlinien \_ Benachrichtigungs \_ Informations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="4261b-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="4261b-118">Definiert die Typen von Richtlinien Informationen und Informationen zur Richtlinien Domäne, für die Ihre Anwendung eine Benachrichtigung über Änderungen anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="4261b-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="4261b-119">**Richtlinien \_ Server \_ \_ Status aktivieren**</span><span class="sxs-lookup"><span data-stu-id="4261b-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="4261b-120">Stellt den Status des LSA-Servers dar, d. h. ob er aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4261b-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="4261b-121">**vertrauenswürdige \_ Informations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="4261b-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="4261b-122">Definiert die Typen von Informationen, die für eine vertrauenswürdige Domäne festgelegt oder abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="4261b-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="4261b-123">Sicherere Enumerationen</span><span class="sxs-lookup"><span data-stu-id="4261b-123">Safer Enumerations</span></span>

<span data-ttu-id="4261b-124">[Sicherer](safer.md) verwendet die folgenden Enumerationstypen.</span><span class="sxs-lookup"><span data-stu-id="4261b-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="4261b-125">Name</span><span class="sxs-lookup"><span data-stu-id="4261b-125">Name</span></span>                                                               | <span data-ttu-id="4261b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4261b-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4261b-127">**sicherere \_ Identifikations \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="4261b-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="4261b-128">Enumerationstyp, der die möglichen Typen von Identifikations Regel Strukturen definiert, die von der [**sicheren \_ Identifikations \_ Header**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) Struktur identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="4261b-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="4261b-129">**sicherere \_ Objekt \_ Informations \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="4261b-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="4261b-130">Enumerationstyp, der den Typ der angeforderten Informationen zu einem sichereren Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="4261b-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="4261b-131">**\_ \_ Informations Klasse der sichereren Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="4261b-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="4261b-132">Enumerationstyp, der die Art und Weise definiert, in der eine Richtlinie abgefragt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4261b-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



