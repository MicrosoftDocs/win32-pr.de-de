---
title: MDM_Policy_User_Result01_Notifications02-Klasse
description: Die MDM \_ - \_ Richt \_ Linien Benutzer Result01 \_ Notifications02-Klasse stellt die verfügbaren Benachrichtigungs Richtlinien dar.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- MDM_Policy_User_Result01_Notifications02-Klasse
- MDM_Policy_User_Result01_Notifications02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c917e42ef568783b1c804ce17d52474a86359e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040148"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a><span data-ttu-id="8248d-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ Notifications02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8248d-105">MDM\_Policy\_User\_Result01\_Notifications02 class</span></span>

<span data-ttu-id="8248d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8248d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8248d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8248d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8248d-108">Die **MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ Notifications02** -Klasse stellt die verfügbaren Benachrichtigungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="8248d-108">The **MDM\_Policy\_User\_Result01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="8248d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8248d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8248d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8248d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="8248d-111">Member</span><span class="sxs-lookup"><span data-stu-id="8248d-111">Members</span></span>

<span data-ttu-id="8248d-112">Die **\_ \_ Benutzer \_ Result01 \_ Notifications02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8248d-112">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="8248d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8248d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8248d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8248d-114">Properties</span></span>

<span data-ttu-id="8248d-115">Die **\_ \_ Benutzer \_ Result01 \_ Notifications02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8248d-115">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8248d-116">Disallownotificationspiegelung</span><span class="sxs-lookup"><span data-stu-id="8248d-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8248d-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8248d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8248d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8248d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8248d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8248d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8248d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8248d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8248d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8248d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8248d-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8248d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8248d-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="8248d-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8248d-124">Für diese Klasse ist die Zeichenfolge "Benachrichtigungen".</span><span class="sxs-lookup"><span data-stu-id="8248d-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="8248d-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8248d-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8248d-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8248d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8248d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8248d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8248d-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8248d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8248d-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="8248d-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="8248d-130">Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="8248d-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8248d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8248d-131">Requirements</span></span>



| <span data-ttu-id="8248d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8248d-132">Requirement</span></span> | <span data-ttu-id="8248d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8248d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8248d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8248d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8248d-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8248d-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8248d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8248d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8248d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8248d-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8248d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8248d-138">Namespace</span></span><br/>                | <span data-ttu-id="8248d-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8248d-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="8248d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8248d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8248d-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8248d-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="8248d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8248d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8248d-143"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="8248d-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

