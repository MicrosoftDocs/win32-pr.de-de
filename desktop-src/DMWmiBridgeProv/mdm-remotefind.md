---
title: MDM_RemoteFind-Klasse
description: Die MDM- \_ remotefind-Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- MDM_RemoteFind-Klasse
- MDM_RemoteFind-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740073"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="d17e6-105">MDM- \_ remotefind-Klasse</span><span class="sxs-lookup"><span data-stu-id="d17e6-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="d17e6-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d17e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d17e6-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d17e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d17e6-108">Die **MDM- \_ remotefind** -Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="d17e6-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="d17e6-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d17e6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d17e6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d17e6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="d17e6-111">Member</span><span class="sxs-lookup"><span data-stu-id="d17e6-111">Members</span></span>

<span data-ttu-id="d17e6-112">Die **MDM- \_ remotefind** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d17e6-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="d17e6-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d17e6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d17e6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d17e6-114">Properties</span></span>

<span data-ttu-id="d17e6-115">Die **MDM- \_ remotefind** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d17e6-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d17e6-116">Desiredaccuracy</span><span class="sxs-lookup"><span data-stu-id="d17e6-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d17e6-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d17e6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d17e6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d17e6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d17e6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d17e6-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d17e6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d17e6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d17e6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d17e6-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="d17e6-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="d17e6-124">Für diese Klasse ist die Zeichenfolge "remotefind".</span><span class="sxs-lookup"><span data-stu-id="d17e6-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="d17e6-125">MaximumAge</span><span class="sxs-lookup"><span data-stu-id="d17e6-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d17e6-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d17e6-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d17e6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d17e6-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d17e6-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d17e6-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d17e6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d17e6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d17e6-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d17e6-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d17e6-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d17e6-133">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="d17e6-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="d17e6-134">Timeout</span><span class="sxs-lookup"><span data-stu-id="d17e6-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d17e6-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d17e6-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d17e6-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d17e6-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d17e6-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d17e6-137">Requirements</span></span>



| <span data-ttu-id="d17e6-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d17e6-138">Requirement</span></span> | <span data-ttu-id="d17e6-139">Wert</span><span class="sxs-lookup"><span data-stu-id="d17e6-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17e6-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d17e6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d17e6-141">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d17e6-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d17e6-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d17e6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d17e6-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d17e6-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d17e6-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="d17e6-144">Namespace</span></span><br/>                | <span data-ttu-id="d17e6-145">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d17e6-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="d17e6-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d17e6-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d17e6-147"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d17e6-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="d17e6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d17e6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d17e6-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d17e6-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d17e6-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d17e6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17e6-151">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="d17e6-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

