---
title: MDM_Policy_Result01_SmartScreen02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ SmartScreen02-Klasse stellt die SmartScreen-Richtlinien dar.
ms.assetid: 9a775712-ce42-48c2-b286-eaf7ca8fed20
keywords:
- MDM_Policy_Result01_SmartScreen02-Klasse
- MDM_Policy_Result01_SmartScreen02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_SmartScreen02
- MDM_Policy_Result01_SmartScreen02.InstanceID
- MDM_Policy_Result01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a49aad764492c54b43327cfb71c0c93fa36870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106227"
---
# <a name="mdm_policy_result01_smartscreen02-class"></a><span data-ttu-id="8b32c-105">MDM- \_ Richtlinie \_ Result01 \_ SmartScreen02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b32c-105">MDM\_Policy\_Result01\_SmartScreen02 class</span></span>

<span data-ttu-id="8b32c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8b32c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8b32c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8b32c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8b32c-108">die MDM- \_ Richtlinie \_ Result01 \_ SmartScreen02-Klasse stellt die SmartScreen-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="8b32c-108">the MDM\_Policy\_Result01\_SmartScreen02 class represents the smart screen policies.</span></span>

<span data-ttu-id="8b32c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8b32c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b32c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b32c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="8b32c-111">Member</span><span class="sxs-lookup"><span data-stu-id="8b32c-111">Members</span></span>

<span data-ttu-id="8b32c-112">Die **MDM- \_ Richtlinie \_ Result01 \_ SmartScreen02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b32c-112">The **MDM\_Policy\_Result01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="8b32c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b32c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b32c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b32c-114">Properties</span></span>

<span data-ttu-id="8b32c-115">Die **MDM- \_ Richtlinie \_ Result01 \_ SmartScreen02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b32c-115">The **MDM\_Policy\_Result01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8b32c-116">Enableappinstallcontrol</span><span class="sxs-lookup"><span data-stu-id="8b32c-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b32c-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b32c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b32c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b32c-119">Enablesmartscreeninshell</span><span class="sxs-lookup"><span data-stu-id="8b32c-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b32c-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b32c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b32c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b32c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8b32c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b32c-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b32c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b32c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b32c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b32c-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8b32c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b32c-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b32c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b32c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b32c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b32c-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="8b32c-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b32c-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b32c-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b32c-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b32c-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b32c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b32c-133">Requirements</span></span>



| <span data-ttu-id="8b32c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b32c-134">Requirement</span></span> | <span data-ttu-id="8b32c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8b32c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b32c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b32c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8b32c-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b32c-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b32c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b32c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8b32c-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b32c-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8b32c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b32c-140">Namespace</span></span><br/>                | <span data-ttu-id="8b32c-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8b32c-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8b32c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8b32c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b32c-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b32c-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b32c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8b32c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b32c-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b32c-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

