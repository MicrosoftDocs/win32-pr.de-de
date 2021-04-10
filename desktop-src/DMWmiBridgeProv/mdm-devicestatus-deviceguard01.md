---
title: MDM_DeviceStatus_DeviceGuard01-Klasse
description: Die MDM \_ DeviceStatus \_ DeviceGuard01-Klasse wird vom Unternehmen verwendet, um den Gerätebestand nachzuverfolgen und den Status der Konformität dieser Geräte mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- MDM_DeviceStatus_DeviceGuard01-Klasse
- MDM_DeviceStatus_DeviceGuard01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956868"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="dee6f-105">MDM \_ DeviceStatus \_ DeviceGuard01-Klasse</span><span class="sxs-lookup"><span data-stu-id="dee6f-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="dee6f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dee6f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dee6f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dee6f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dee6f-108">Die MDM \_ DeviceStatus \_ DeviceGuard01-Klasse wird vom Unternehmen verwendet, um den Gerätebestand nachzuverfolgen und den Status der Konformität dieser Geräte mit ihren Unternehmensrichtlinien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="dee6f-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="dee6f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dee6f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee6f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dee6f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="dee6f-111">Member</span><span class="sxs-lookup"><span data-stu-id="dee6f-111">Members</span></span>

<span data-ttu-id="dee6f-112">Die **MDM \_ DeviceStatus \_ DeviceGuard01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dee6f-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="dee6f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dee6f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dee6f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dee6f-114">Properties</span></span>

<span data-ttu-id="dee6f-115">Die **MDM \_ DeviceStatus \_ DeviceGuard01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dee6f-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dee6f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dee6f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee6f-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dee6f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dee6f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dee6f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dee6f-120">Lsacfgkredguardstatus</span><span class="sxs-lookup"><span data-stu-id="dee6f-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee6f-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dee6f-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dee6f-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dee6f-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dee6f-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee6f-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dee6f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dee6f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dee6f-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dee6f-127">Virtualizationbasedsecurityhwreq</span><span class="sxs-lookup"><span data-stu-id="dee6f-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee6f-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dee6f-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dee6f-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dee6f-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="dee6f-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee6f-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dee6f-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee6f-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dee6f-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dee6f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dee6f-133">Requirements</span></span>



| <span data-ttu-id="dee6f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dee6f-134">Requirement</span></span> | <span data-ttu-id="dee6f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="dee6f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee6f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dee6f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dee6f-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dee6f-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dee6f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dee6f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dee6f-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dee6f-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dee6f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="dee6f-140">Namespace</span></span><br/>                | <span data-ttu-id="dee6f-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dee6f-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dee6f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dee6f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dee6f-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dee6f-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dee6f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dee6f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee6f-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee6f-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

