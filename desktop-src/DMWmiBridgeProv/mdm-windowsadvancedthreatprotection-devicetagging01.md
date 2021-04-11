---
title: MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse
description: Die MDM \_ windowsadvancedfixprotection \_ DeviceTagging01-Klasse wird verwendet, um die Integration, den Konfigurations-und Integritäts Status und die offboardendpunkte für Windows Defender Advanced Threat Protection zu integrieren.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104943"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="33aa3-105">MDM \_ windowsadvancedo Protection \_ DeviceTagging01-Klasse</span><span class="sxs-lookup"><span data-stu-id="33aa3-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="33aa3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="33aa3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33aa3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="33aa3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33aa3-108">Die MDM \_ windowsadvancedfixprotection \_ DeviceTagging01-Klasse wird verwendet, um die Integration, den Konfigurations-und Integritäts Status und die offboardendpunkte für Windows Defender Advanced Threat Protection zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="33aa3-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="33aa3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="33aa3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33aa3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="33aa3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="33aa3-111">Member</span><span class="sxs-lookup"><span data-stu-id="33aa3-111">Members</span></span>

<span data-ttu-id="33aa3-112">Die **MDM \_ windowsadvancedo Protection \_ DeviceTagging01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="33aa3-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="33aa3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33aa3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33aa3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33aa3-114">Properties</span></span>

<span data-ttu-id="33aa3-115">Die **MDM \_ windowsadvancedbedrohlich Protection \_ DeviceTagging01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="33aa3-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33aa3-116">Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="33aa3-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33aa3-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33aa3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33aa3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33aa3-119">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="33aa3-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33aa3-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="33aa3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33aa3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33aa3-122">**Idmethod**</span><span class="sxs-lookup"><span data-stu-id="33aa3-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33aa3-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33aa3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="33aa3-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="33aa3-125">TBD</span><span class="sxs-lookup"><span data-stu-id="33aa3-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="33aa3-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33aa3-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33aa3-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="33aa3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33aa3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33aa3-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33aa3-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="33aa3-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33aa3-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="33aa3-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="33aa3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33aa3-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33aa3-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33aa3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33aa3-134">Requirements</span></span>



| <span data-ttu-id="33aa3-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33aa3-135">Requirement</span></span> | <span data-ttu-id="33aa3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="33aa3-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33aa3-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33aa3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="33aa3-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33aa3-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33aa3-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33aa3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="33aa3-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="33aa3-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="33aa3-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="33aa3-141">Namespace</span></span><br/>                | <span data-ttu-id="33aa3-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="33aa3-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="33aa3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="33aa3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33aa3-144"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="33aa3-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="33aa3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="33aa3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33aa3-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33aa3-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

