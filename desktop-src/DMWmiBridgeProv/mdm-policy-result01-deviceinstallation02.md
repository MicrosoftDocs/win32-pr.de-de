---
title: MDM_Policy_Result01_DeviceInstallation02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ DeviceInstallation02-Klasse stellt die verfügbaren Geräte Installationsrichtlinien dar.
ms.assetid: a5c89661-16f1-42e7-a11d-2c3a7945dac3
keywords:
- MDM_Policy_Result01_DeviceInstallation02-Klasse
- MDM_Policy_Result01_DeviceInstallation02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceInstallation02
- MDM_Policy_Result01_DeviceInstallation02.InstanceID
- MDM_Policy_Result01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6ec11cbfc5b0b38aa5e7482507108204b8798d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949586"
---
# <a name="mdm_policy_result01_deviceinstallation02-class"></a><span data-ttu-id="7a08d-105">MDM- \_ Richtlinie \_ Result01 \_ DeviceInstallation02-Klasse</span><span class="sxs-lookup"><span data-stu-id="7a08d-105">MDM\_Policy\_Result01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="7a08d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7a08d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7a08d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7a08d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7a08d-108">Die MDM- \_ Richtlinie \_ Result01 \_ DeviceInstallation02-Klasse stellt die verfügbaren Geräte Installationsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="7a08d-108">The MDM\_Policy\_Result01\_DeviceInstallation02 class represents the available device installation policies.</span></span>

<span data-ttu-id="7a08d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7a08d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a08d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a08d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="7a08d-111">Member</span><span class="sxs-lookup"><span data-stu-id="7a08d-111">Members</span></span>

<span data-ttu-id="7a08d-112">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceInstallation02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7a08d-112">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="7a08d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a08d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a08d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a08d-114">Properties</span></span>

<span data-ttu-id="7a08d-115">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceInstallation02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a08d-115">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a08d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7a08d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a08d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a08d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a08d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a08d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7a08d-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7a08d-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a08d-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a08d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a08d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a08d-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7a08d-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="7a08d-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a08d-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a08d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a08d-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7a08d-127">Preventinstallationofmatchingtovicesetupclasses</span><span class="sxs-lookup"><span data-stu-id="7a08d-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a08d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a08d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a08d-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a08d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a08d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a08d-130">Requirements</span></span>



| <span data-ttu-id="7a08d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a08d-131">Requirement</span></span> | <span data-ttu-id="7a08d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7a08d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a08d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a08d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7a08d-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a08d-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a08d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a08d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7a08d-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a08d-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7a08d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a08d-137">Namespace</span></span><br/>                | <span data-ttu-id="7a08d-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7a08d-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7a08d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7a08d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a08d-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a08d-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a08d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7a08d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a08d-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a08d-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

