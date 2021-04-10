---
title: MDM_Policy_Config01_DeviceInstallation02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ DeviceInstallation02-Klasse konfiguriert die verfügbaren Geräte Installationsrichtlinien.
ms.assetid: 6aa60809-d6c7-4dfb-9144-e5d69466f454
keywords:
- MDM_Policy_Config01_DeviceInstallation02-Klasse
- MDM_Policy_Config01_DeviceInstallation02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceInstallation02
- MDM_Policy_Config01_DeviceInstallation02.InstanceID
- MDM_Policy_Config01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79df6829f05a49ff5f16e3d8e0cd3dfabfc7bbf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858780"
---
# <a name="mdm_policy_config01_deviceinstallation02-class"></a><span data-ttu-id="fe2ec-105">MDM- \_ Richtlinie \_ Config01 \_ DeviceInstallation02-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe2ec-105">MDM\_Policy\_Config01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="fe2ec-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fe2ec-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="fe2ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fe2ec-108">Die MDM- \_ Richtlinie \_ Config01 \_ DeviceInstallation02-Klasse konfiguriert die verfügbaren Geräte Installationsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-108">The MDM\_Policy\_Config01\_DeviceInstallation02 class configures the available device installation policies.</span></span>

<span data-ttu-id="fe2ec-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2ec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe2ec-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="fe2ec-111">Member</span><span class="sxs-lookup"><span data-stu-id="fe2ec-111">Members</span></span>

<span data-ttu-id="fe2ec-112">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceInstallation02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe2ec-112">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="fe2ec-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe2ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe2ec-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe2ec-114">Properties</span></span>

<span data-ttu-id="fe2ec-115">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceInstallation02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-115">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe2ec-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe2ec-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe2ec-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe2ec-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe2ec-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe2ec-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe2ec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe2ec-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe2ec-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="fe2ec-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe2ec-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fe2ec-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe2ec-127">Preventinstallationofmatchingtovicesetupclasses</span><span class="sxs-lookup"><span data-stu-id="fe2ec-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe2ec-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe2ec-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe2ec-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fe2ec-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe2ec-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe2ec-130">Requirements</span></span>



| <span data-ttu-id="fe2ec-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe2ec-131">Requirement</span></span> | <span data-ttu-id="fe2ec-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fe2ec-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2ec-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe2ec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2ec-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe2ec-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe2ec-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe2ec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2ec-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe2ec-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fe2ec-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe2ec-137">Namespace</span></span><br/>                | <span data-ttu-id="fe2ec-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fe2ec-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fe2ec-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fe2ec-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe2ec-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe2ec-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe2ec-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fe2ec-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe2ec-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe2ec-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

