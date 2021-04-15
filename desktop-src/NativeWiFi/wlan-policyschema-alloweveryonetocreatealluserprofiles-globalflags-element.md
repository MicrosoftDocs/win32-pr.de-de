---
description: Gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: "' zugweveryonetkreatealluserprofiles '-Element (globalflags)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525766"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="0a6cc-103">' zugweveryonetkreatealluserprofiles '-Element (globalflags)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="0a6cc-104">Das Element " **connecweveryonedekreatealluserprofiles** " (globalflags) gibt an, ob ein Benutzer ein Profil für alle Benutzer erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="0a6cc-105">Ein Profil für alle Benutzer kann von jedem Benutzer auf dem Computer verwendet werden, um eine Verbindung mit dem Drahtlos Netzwerk herzustellen, das mit dem Profil verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="0a6cc-106">Wenn "zugebestellungs-Manager- **profile** " auf "true" festgelegt ist, kann ein beliebiges Benutzerprofil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="0a6cc-107">Wenn " **connecweveryonedekreatealluserprofiles** " auf "false" festgelegt ist, können nicht alle Benutzer ein Profil für alle Benutzer erstellen, und es gibt eine DACL, die dem \_ Sicherheits Objekt "WLAN Secure \_ Add New all User Profiles" zugeordnet ist, \_ \_ \_ \_ das die Benutzer oder Benutzergruppen mit der Berechtigung zum Erstellen von Profilen für alle Benutzer angibt.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="0a6cc-108">Die Standard-DACL gibt an, dass nur Benutzer, die als Mitglied der Gruppe "Administratoren" angemeldet sind, ein Profil für alle Benutzer erstellen können.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="0a6cc-109">Die Standard Sicherheitseinstellungen können durch Aufrufen von [**wlansetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="0a6cc-110">Um die aktuellen Sicherheitseinstellungen abzurufen, nennen Sie [**wlangetsecuritysettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="0a6cc-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="0a6cc-111">Dieses Element ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-111">This element is mandatory.</span></span> <span data-ttu-id="0a6cc-112">Wenn ein Profil vom AutoConfig-Dienst erstellt wird, hat dieses Element den Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="0a6cc-113">Das Element " **connecweveryonetkreatealluserprofiles** " wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6cc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a6cc-114">Requirements</span></span>



| <span data-ttu-id="0a6cc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a6cc-115">Requirement</span></span> | <span data-ttu-id="0a6cc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0a6cc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a6cc-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6cc-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a6cc-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a6cc-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6cc-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a6cc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a6cc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a6cc-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a6cc-122">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="0a6cc-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0a6cc-123">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="0a6cc-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="0a6cc-124">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="0a6cc-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0a6cc-125">**globalflags (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="0a6cc-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




