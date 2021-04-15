---
title: MDM_DeviceStatus_Antivirus01-Klasse
description: Die MDM \_ DeviceStatus \_ Antivirus01-Klasse wird vom Unternehmen verwendet, um den Status der Antivirenkonformität von Geräten mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: 8b3145a6-b836-4750-a0c3-88472f9a12c5
keywords:
- MDM_DeviceStatus_Antivirus01-Klasse
- MDM_DeviceStatus_Antivirus01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antivirus01
- MDM_DeviceStatus_Antivirus01.InstanceID
- MDM_DeviceStatus_Antivirus01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3197dddb9bea498de63d08a025050963d4348054
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478078"
---
# <a name="mdm_devicestatus_antivirus01-class"></a><span data-ttu-id="0805a-105">MDM \_ DeviceStatus \_ Antivirus01-Klasse</span><span class="sxs-lookup"><span data-stu-id="0805a-105">MDM\_DeviceStatus\_Antivirus01 class</span></span>

<span data-ttu-id="0805a-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0805a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0805a-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0805a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0805a-108">Die **MDM \_ DeviceStatus \_ Antivirus01** -Klasse wird vom Unternehmen verwendet, um den Status der Antivirenkonformität von Geräten mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0805a-108">The **MDM\_DeviceStatus\_Antivirus01** class is used by the enterprise to query the state of antivirus compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="0805a-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0805a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0805a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0805a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antivirus01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="0805a-111">Member</span><span class="sxs-lookup"><span data-stu-id="0805a-111">Members</span></span>

<span data-ttu-id="0805a-112">Die **MDM \_ DeviceStatus \_ Antivirus01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0805a-112">The **MDM\_DeviceStatus\_Antivirus01** class has these types of members:</span></span>

-   [<span data-ttu-id="0805a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0805a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0805a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0805a-114">Properties</span></span>

<span data-ttu-id="0805a-115">Die **MDM \_ DeviceStatus \_ Antivirus01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0805a-115">The **MDM\_DeviceStatus\_Antivirus01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0805a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0805a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0805a-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0805a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0805a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0805a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0805a-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0805a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0805a-120">Der Knoten für die antivirenabfrage.</span><span class="sxs-lookup"><span data-stu-id="0805a-120">Node for the antivirus query.</span></span>

</dd> <dt>

<span data-ttu-id="0805a-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0805a-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0805a-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0805a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0805a-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0805a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0805a-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0805a-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0805a-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0805a-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="0805a-126">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="0805a-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="0805a-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="0805a-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0805a-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0805a-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0805a-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0805a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0805a-130">Status</span><span class="sxs-lookup"><span data-stu-id="0805a-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0805a-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0805a-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0805a-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0805a-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0805a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0805a-133">Requirements</span></span>



| <span data-ttu-id="0805a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0805a-134">Requirement</span></span> | <span data-ttu-id="0805a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0805a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0805a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0805a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0805a-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0805a-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0805a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0805a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0805a-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0805a-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0805a-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="0805a-140">Namespace</span></span><br/>                | <span data-ttu-id="0805a-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0805a-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0805a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0805a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0805a-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0805a-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0805a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0805a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0805a-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0805a-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

