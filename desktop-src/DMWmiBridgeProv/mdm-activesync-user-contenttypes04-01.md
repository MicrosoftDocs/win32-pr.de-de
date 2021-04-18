---
title: MDM_ActiveSync_User_ContentTypes04_01-Klasse
description: Die MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01-Klasse definiert den Typ des Inhalts, der einzeln für die Synchronisierung aktiviert bzw. deaktiviert werden soll.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- MDM_ActiveSync_User_ContentTypes04_01-Klasse
- MDM_ActiveSync_User_ContentTypes04_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337734"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="211e2-105">MDM \_ ActiveSync- \_ Benutzer \_ ContentTypes04 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="211e2-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="211e2-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="211e2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="211e2-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="211e2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="211e2-108">Die **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** -Klasse definiert den Typ des Inhalts, der einzeln für die Synchronisierung aktiviert bzw. deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="211e2-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="211e2-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="211e2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="211e2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="211e2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="211e2-111">Member</span><span class="sxs-lookup"><span data-stu-id="211e2-111">Members</span></span>

<span data-ttu-id="211e2-112">Die **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="211e2-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="211e2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211e2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="211e2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211e2-114">Properties</span></span>

<span data-ttu-id="211e2-115">Die **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="211e2-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="211e2-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="211e2-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211e2-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211e2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211e2-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211e2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211e2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="211e2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211e2-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211e2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211e2-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="211e2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211e2-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="211e2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="211e2-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="211e2-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="211e2-124">Name</span><span class="sxs-lookup"><span data-stu-id="211e2-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="211e2-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211e2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211e2-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="211e2-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="211e2-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="211e2-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211e2-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="211e2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211e2-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="211e2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211e2-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="211e2-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="211e2-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="211e2-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="211e2-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options".</span><span class="sxs-lookup"><span data-stu-id="211e2-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="211e2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="211e2-133">Requirements</span></span>



| <span data-ttu-id="211e2-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="211e2-134">Requirement</span></span> | <span data-ttu-id="211e2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="211e2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="211e2-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="211e2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="211e2-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="211e2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="211e2-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="211e2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="211e2-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="211e2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="211e2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="211e2-140">Namespace</span></span><br/>                | <span data-ttu-id="211e2-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="211e2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="211e2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="211e2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="211e2-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="211e2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="211e2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="211e2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211e2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211e2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211e2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="211e2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211e2-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="211e2-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

