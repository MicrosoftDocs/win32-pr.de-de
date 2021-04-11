---
title: MDM_DeviceStatus_Compliance01-Klasse
description: Mit der MDM \_ DeviceStatus \_ Compliance01-Klasse können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- MDM_DeviceStatus_Compliance01-Klasse
- MDM_DeviceStatus_Compliance01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105008"
---
# <a name="mdm_devicestatus_compliance01-class"></a><span data-ttu-id="f0737-105">MDM \_ DeviceStatus \_ Compliance01-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0737-105">MDM\_DeviceStatus\_Compliance01 class</span></span>

<span data-ttu-id="f0737-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f0737-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0737-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f0737-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0737-108">Mit der **MDM \_ DeviceStatus \_ Compliance01** -Klasse können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.</span><span class="sxs-lookup"><span data-stu-id="f0737-108">The **MDM\_DeviceStatus\_Compliance01** class allows you to query whether device are in compliance with enterprise encryption policy.</span></span>

<span data-ttu-id="f0737-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f0737-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0737-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0737-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a><span data-ttu-id="f0737-111">Member</span><span class="sxs-lookup"><span data-stu-id="f0737-111">Members</span></span>

<span data-ttu-id="f0737-112">Die **MDM \_ DeviceStatus \_ Compliance01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f0737-112">The **MDM\_DeviceStatus\_Compliance01** class has these types of members:</span></span>

-   [<span data-ttu-id="f0737-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0737-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0737-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0737-114">Properties</span></span>

<span data-ttu-id="f0737-115">Die **MDM \_ DeviceStatus \_ Compliance01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0737-115">The **MDM\_DeviceStatus\_Compliance01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f0737-116">Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="f0737-116">EncryptionCompliance</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0737-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f0737-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0737-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f0737-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0737-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0737-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0737-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0737-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0737-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0737-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0737-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0737-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0737-123">Knoten für Kompatibilitäts Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f0737-123">Node for queries on compliance.</span></span>

</dd> <dt>

<span data-ttu-id="f0737-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f0737-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0737-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f0737-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0737-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f0737-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0737-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0737-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0737-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="f0737-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="f0737-129">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="f0737-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0737-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0737-130">Requirements</span></span>



| <span data-ttu-id="f0737-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0737-131">Requirement</span></span> | <span data-ttu-id="f0737-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f0737-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0737-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0737-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f0737-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0737-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0737-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0737-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f0737-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0737-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f0737-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0737-137">Namespace</span></span><br/>                | <span data-ttu-id="f0737-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f0737-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f0737-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f0737-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0737-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0737-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0737-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f0737-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0737-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0737-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0737-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0737-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0737-144">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="f0737-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

