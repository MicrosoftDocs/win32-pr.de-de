---
description: Listet die Zugriffs Typen des Policy-Objekts auf und beschreibt diese.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Zugriffsrechte für Richtlinien Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346295"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="1ae74-103">Zugriffsrechte für Richtlinien Objekte</span><span class="sxs-lookup"><span data-stu-id="1ae74-103">Policy Object Access Rights</span></span>

<span data-ttu-id="1ae74-104">Das [**Policy**](policy-object.md) -Objekt verfügt über die folgenden Objekt spezifischen Zugriffs Typen:</span><span class="sxs-lookup"><span data-stu-id="1ae74-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="1ae74-105">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1ae74-105">Access type</span></span>                         | <span data-ttu-id="1ae74-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ae74-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae74-107">\_ \_ lokale \_ Informationen zur Richtlinien Anzeige</span><span class="sxs-lookup"><span data-stu-id="1ae74-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="1ae74-108">Dieser Zugriffstyp ist erforderlich, um die verschiedenen Sicherheitsrichtlinien Informationen des Zielsystems zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1ae74-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="1ae74-109">Dies umfasst das Standard Kontingent, die Überwachung, den Serverstatus und die Informationen zur Rolle sowie Informationen zur Vertrauensstellung.</span><span class="sxs-lookup"><span data-stu-id="1ae74-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="1ae74-110">Dieser Zugriffstyp wird auch zum Auflisten vertrauenswürdiger Domänen, Konten und [*Berechtigungen*](/windows/desktop/SecGloss/p-gly)benötigt.</span><span class="sxs-lookup"><span data-stu-id="1ae74-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="1ae74-111">Richtlinie \_ get \_ private \_ Information</span><span class="sxs-lookup"><span data-stu-id="1ae74-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="1ae74-112">Dieser Zugriffstyp ist erforderlich, um vertrauliche Informationen anzuzeigen, z. b. die Namen der Konten, die für vertrauenswürdige Domänen Beziehungen hergestellt wurden</span><span class="sxs-lookup"><span data-stu-id="1ae74-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="1ae74-113">Richtlinien \_ Vertrauensstellungs \_ Administrator</span><span class="sxs-lookup"><span data-stu-id="1ae74-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="1ae74-114">Dieser Zugriffstyp ist erforderlich, um die Informationen zur Konto Domäne oder zur primären Domäne zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1ae74-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1ae74-115">\_ \_ Standard \_ Kontingent \_ Limits für Richtlinien festlegen</span><span class="sxs-lookup"><span data-stu-id="1ae74-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="1ae74-116">Legen Sie die standardmäßigen System Kontingente fest, die auf Benutzerkonten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ae74-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1ae74-117">Richtlinie \_ Create \_ Secret</span><span class="sxs-lookup"><span data-stu-id="1ae74-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="1ae74-118">Dieser Zugriffstyp ist erforderlich, um ein neues privates Datenobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1ae74-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1ae74-119">Konto für die Richtlinien \_ Erstellung \_</span><span class="sxs-lookup"><span data-stu-id="1ae74-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="1ae74-120">Dieser Zugriffstyp wird zum Erstellen eines neuen [**Konto**](account-object.md) Objekts benötigt.</span><span class="sxs-lookup"><span data-stu-id="1ae74-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1ae74-121">Richtlinien \_ Satz-Überwachungs \_ \_ Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ae74-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="1ae74-122">Dieser Zugriffstyp ist erforderlich, um die Überwachungsanforderungen des Systems zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1ae74-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1ae74-123">Richtlinien \_ Überwachungs \_ Protokoll- \_ Administrator</span><span class="sxs-lookup"><span data-stu-id="1ae74-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="1ae74-124">Dieser Zugriffstyp wird benötigt, um die Eigenschaften des Überwachungs Pfads zu ändern, z. b. die maximale Größe oder die Beibehaltungs Dauer für Überwachungsdaten Sätze, oder um das Protokoll zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1ae74-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="1ae74-125">Überwachungsinformationen für die Richtlinien \_ Ansicht \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ae74-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="1ae74-126">Dieser Zugriffstyp ist erforderlich, um Informationen über Überwachungs Pfade oder Überwachungsanforderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1ae74-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1ae74-127">Richtlinien \_ Server \_ Administrator</span><span class="sxs-lookup"><span data-stu-id="1ae74-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="1ae74-128">Dieser Zugriffstyp ist erforderlich, um die Informationen zum Serverstatus oder zur Rolle (Master/Replica) zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1ae74-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="1ae74-129">Außerdem müssen die Informationen zur Replikat Quelle und zum Kontonamen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1ae74-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="1ae74-130">Namen der Richtlinien \_ Suche \_</span><span class="sxs-lookup"><span data-stu-id="1ae74-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="1ae74-131">Dieser Zugriffstyp ist erforderlich, um zwischen Namen und SIDs zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="1ae74-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1ae74-132">\_ \_ Berechtigungs Erstellungs Berechtigung</span><span class="sxs-lookup"><span data-stu-id="1ae74-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="1ae74-133">Noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ae74-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="1ae74-134">Generische Zugriffs Masken</span><span class="sxs-lookup"><span data-stu-id="1ae74-134">Generic Access Masks</span></span>

<span data-ttu-id="1ae74-135">Das [**Policy**](policy-object.md) -Objekt veröffentlicht die folgenden Zuordnungen von generischen Zugriffs Typen auf bestimmte Zugriffs Typen:</span><span class="sxs-lookup"><span data-stu-id="1ae74-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="1ae74-136">Standard Zugriffs Typen</span><span class="sxs-lookup"><span data-stu-id="1ae74-136">Standard Access Types</span></span>

<span data-ttu-id="1ae74-137">Dieses Objekt unterstützt den (optionalen) Standard Zugriffstyp "synchronisieren" nicht.</span><span class="sxs-lookup"><span data-stu-id="1ae74-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="1ae74-138">Alle erforderlichen Zugriffs Typen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ae74-138">All required access types are supported.</span></span> <span data-ttu-id="1ae74-139">Die Maske aller unterstützten Zugriffs Typen für diesen Objekttyp lautet:</span><span class="sxs-lookup"><span data-stu-id="1ae74-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
