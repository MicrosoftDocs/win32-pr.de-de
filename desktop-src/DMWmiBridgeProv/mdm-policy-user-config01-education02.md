---
title: MDM_Policy_User_Config01_Education02-Klasse
description: Die Richtlinien für die MDM- \_ Richtlinie \_ User \_ Config01 \_ Education02 konfiguriert die Education-Richtlinien.
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- MDM_Policy_User_Config01_Education02-Klasse
- MDM_Policy_User_Config01_Education02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae8508668b95edce1d4c4a2d0e99cbba2bc6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949585"
---
# <a name="mdm_policy_user_config01_education02-class"></a><span data-ttu-id="85d02-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ Education02-Klasse</span><span class="sxs-lookup"><span data-stu-id="85d02-105">MDM\_Policy\_User\_Config01\_Education02 class</span></span>

<span data-ttu-id="85d02-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="85d02-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="85d02-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="85d02-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="85d02-108">Die Richtlinien für die MDM- \_ Richtlinie \_ User \_ Config01 \_ Education02 konfiguriert die Education-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="85d02-108">The MDM\_Policy\_User\_Config01\_Education02 class configures the education policies.</span></span>

<span data-ttu-id="85d02-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="85d02-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d02-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d02-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="85d02-111">Member</span><span class="sxs-lookup"><span data-stu-id="85d02-111">Members</span></span>

<span data-ttu-id="85d02-112">Die **\_ \_ Benutzer \_ Config01 \_ Education02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85d02-112">The **MDM\_Policy\_User\_Config01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="85d02-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85d02-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85d02-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85d02-114">Properties</span></span>

<span data-ttu-id="85d02-115">Die **\_ \_ Benutzer \_ Config01 \_ Education02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85d02-115">The **MDM\_Policy\_User\_Config01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="85d02-116">Defaultprintername</span><span class="sxs-lookup"><span data-stu-id="85d02-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d02-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85d02-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85d02-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85d02-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85d02-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85d02-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d02-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85d02-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85d02-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85d02-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d02-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85d02-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85d02-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="85d02-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d02-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85d02-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85d02-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85d02-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85d02-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85d02-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="85d02-127">Preventaddingnewprinter</span><span class="sxs-lookup"><span data-stu-id="85d02-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d02-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="85d02-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="85d02-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85d02-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="85d02-130">Printernames</span><span class="sxs-lookup"><span data-stu-id="85d02-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85d02-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85d02-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85d02-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85d02-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85d02-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85d02-133">Requirements</span></span>



| <span data-ttu-id="85d02-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85d02-134">Requirement</span></span> | <span data-ttu-id="85d02-135">Wert</span><span class="sxs-lookup"><span data-stu-id="85d02-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85d02-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85d02-136">Minimum supported client</span></span><br/> | <span data-ttu-id="85d02-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85d02-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85d02-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85d02-138">Minimum supported server</span></span><br/> | <span data-ttu-id="85d02-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85d02-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="85d02-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="85d02-140">Namespace</span></span><br/>                | <span data-ttu-id="85d02-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="85d02-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="85d02-142">MOF</span><span class="sxs-lookup"><span data-stu-id="85d02-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85d02-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85d02-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="85d02-144">DLL</span><span class="sxs-lookup"><span data-stu-id="85d02-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85d02-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85d02-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

