---
title: MDM_Policy_Config01_SmartScreen02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ SmartScreen02-Klasse konfiguriert die Richtlinien für den intelligenten Bildschirm.
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- MDM_Policy_Config01_SmartScreen02-Klasse
- MDM_Policy_Config01_SmartScreen02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e0b8ca0c1e53005ab2a2ab80cce3f18dec40b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040660"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a><span data-ttu-id="5626d-105">MDM- \_ Richtlinie \_ Config01 \_ SmartScreen02-Klasse</span><span class="sxs-lookup"><span data-stu-id="5626d-105">MDM\_Policy\_Config01\_SmartScreen02 class</span></span>

<span data-ttu-id="5626d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="5626d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5626d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="5626d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5626d-108">Die MDM- \_ Richtlinie \_ Config01 \_ SmartScreen02-Klasse konfiguriert die Richtlinien für den intelligenten Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="5626d-108">The MDM\_Policy\_Config01\_SmartScreen02 class configures the smart screen policies.</span></span>

<span data-ttu-id="5626d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5626d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5626d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5626d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="5626d-111">Member</span><span class="sxs-lookup"><span data-stu-id="5626d-111">Members</span></span>

<span data-ttu-id="5626d-112">Die **MDM- \_ Richtlinie \_ Config01 \_ SmartScreen02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5626d-112">The **MDM\_Policy\_Config01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="5626d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5626d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5626d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5626d-114">Properties</span></span>

<span data-ttu-id="5626d-115">Die **MDM- \_ Richtlinie \_ Config01 \_ SmartScreen02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5626d-115">The **MDM\_Policy\_Config01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5626d-116">Enableappinstallcontrol</span><span class="sxs-lookup"><span data-stu-id="5626d-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5626d-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5626d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5626d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5626d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5626d-119">Enablesmartscreeninshell</span><span class="sxs-lookup"><span data-stu-id="5626d-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5626d-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5626d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5626d-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5626d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5626d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5626d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5626d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5626d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5626d-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5626d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5626d-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5626d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5626d-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5626d-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5626d-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5626d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5626d-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5626d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5626d-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5626d-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5626d-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="5626d-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5626d-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5626d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5626d-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5626d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5626d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5626d-133">Requirements</span></span>



| <span data-ttu-id="5626d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5626d-134">Requirement</span></span> | <span data-ttu-id="5626d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5626d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5626d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5626d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5626d-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5626d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5626d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5626d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5626d-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5626d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5626d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5626d-140">Namespace</span></span><br/>                | <span data-ttu-id="5626d-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="5626d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5626d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5626d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5626d-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5626d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5626d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5626d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5626d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5626d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

