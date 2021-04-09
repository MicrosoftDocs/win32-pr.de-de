---
title: MDM_DeviceStatus-Klasse
description: Die MDM \_ DeviceStatus-Klasse wird vom Unternehmen verwendet, um die Geräte Inventur nachzuverfolgen und den Status der Konformität dieser Geräte mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: fceaaf36-8f33-410a-89b4-c824b10164d5
keywords:
- MDM_DeviceStatus-Klasse
- MDM_DeviceStatus-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus
- MDM_DeviceStatus.InstanceID
- MDM_DeviceStatus.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751a33553b4a00ac6719ce6e24c75a03444f0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104996"
---
# <a name="mdm_devicestatus-class"></a><span data-ttu-id="85236-105">MDM \_ DeviceStatus-Klasse</span><span class="sxs-lookup"><span data-stu-id="85236-105">MDM\_DeviceStatus class</span></span>

<span data-ttu-id="85236-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="85236-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="85236-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="85236-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="85236-108">Die **MDM \_ DeviceStatus** -Klasse wird vom Unternehmen verwendet, um die Geräte Inventur nachzuverfolgen und den Status der Konformität dieser Geräte mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="85236-108">The **MDM\_DeviceStatus** class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="85236-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="85236-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85236-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="85236-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus
{
  string InstanceID;
  string ParentID;
  sint32 SecureBootState;
  string DomainName;
};
```

## <a name="members"></a><span data-ttu-id="85236-111">Member</span><span class="sxs-lookup"><span data-stu-id="85236-111">Members</span></span>

<span data-ttu-id="85236-112">Die **MDM \_ DeviceStatus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85236-112">The **MDM\_DeviceStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="85236-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85236-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85236-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85236-114">Properties</span></span>

<span data-ttu-id="85236-115">Die **MDM \_ DeviceStatus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85236-115">The **MDM\_DeviceStatus** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="85236-116">DomainName</span><span class="sxs-lookup"><span data-stu-id="85236-116">DomainName</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85236-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85236-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85236-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85236-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85236-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85236-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85236-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85236-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85236-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85236-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85236-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85236-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85236-123">Der Stamm Knoten für den DeviceStatus-Konfigurations Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="85236-123">The root node for the DeviceStatus configuration service provider.</span></span>

</dd> <dt>

<span data-ttu-id="85236-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="85236-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85236-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85236-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85236-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85236-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85236-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85236-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85236-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="85236-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="85236-129">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="85236-129">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="85236-130">Securebootstate</span><span class="sxs-lookup"><span data-stu-id="85236-130">SecureBootState</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-securebootstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85236-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="85236-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="85236-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85236-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85236-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85236-133">Requirements</span></span>



| <span data-ttu-id="85236-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85236-134">Requirement</span></span> | <span data-ttu-id="85236-135">Wert</span><span class="sxs-lookup"><span data-stu-id="85236-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85236-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85236-136">Minimum supported client</span></span><br/> | <span data-ttu-id="85236-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85236-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85236-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85236-138">Minimum supported server</span></span><br/> | <span data-ttu-id="85236-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85236-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="85236-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="85236-140">Namespace</span></span><br/>                | <span data-ttu-id="85236-141">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="85236-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="85236-142">MOF</span><span class="sxs-lookup"><span data-stu-id="85236-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85236-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85236-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="85236-144">DLL</span><span class="sxs-lookup"><span data-stu-id="85236-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85236-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85236-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85236-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85236-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85236-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="85236-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

