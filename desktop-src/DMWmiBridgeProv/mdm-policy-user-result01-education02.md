---
title: MDM_Policy_User_Result01_Education02-Klasse
description: Die Benutzer Result01 Education02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die Bildungsrichtlinien dar.
ms.assetid: 34dcc478-5f39-4e1a-908b-46cbbf2ff4fd
keywords:
- MDM_Policy_User_Result01_Education02-Klasse
- MDM_Policy_User_Result01_Education02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Education02
- MDM_Policy_User_Result01_Education02.InstanceID
- MDM_Policy_User_Result01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce82ae1131287ec04c77e084e822609a0e0ab07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391943"
---
# <a name="mdm_policy_user_result01_education02-class"></a><span data-ttu-id="fe672-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ Education02-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe672-105">MDM\_Policy\_User\_Result01\_Education02 class</span></span>

<span data-ttu-id="fe672-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fe672-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fe672-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="fe672-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fe672-108">Die Benutzer Result01 Education02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die Bildungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="fe672-108">The MDM\_Policy\_User\_Result01\_Education02 class represents the education policies.</span></span>

<span data-ttu-id="fe672-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fe672-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe672-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe672-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="fe672-111">Member</span><span class="sxs-lookup"><span data-stu-id="fe672-111">Members</span></span>

<span data-ttu-id="fe672-112">Die **\_ \_ Benutzer \_ Result01 \_ Education02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe672-112">The **MDM\_Policy\_User\_Result01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="fe672-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe672-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe672-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe672-114">Properties</span></span>

<span data-ttu-id="fe672-115">Die **\_ \_ Benutzer \_ Result01 \_ Education02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe672-115">The **MDM\_Policy\_User\_Result01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fe672-116">Defaultprintername</span><span class="sxs-lookup"><span data-stu-id="fe672-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe672-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe672-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe672-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fe672-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe672-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe672-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe672-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe672-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe672-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe672-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe672-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe672-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe672-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fe672-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe672-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe672-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe672-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe672-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe672-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe672-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe672-127">Preventaddingnewprinter</span><span class="sxs-lookup"><span data-stu-id="fe672-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe672-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fe672-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe672-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fe672-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe672-130">Printernames</span><span class="sxs-lookup"><span data-stu-id="fe672-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe672-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fe672-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe672-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fe672-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe672-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe672-133">Requirements</span></span>



| <span data-ttu-id="fe672-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe672-134">Requirement</span></span> | <span data-ttu-id="fe672-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fe672-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe672-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe672-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fe672-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe672-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe672-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe672-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fe672-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fe672-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fe672-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe672-140">Namespace</span></span><br/>                | <span data-ttu-id="fe672-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fe672-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fe672-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fe672-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe672-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe672-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe672-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fe672-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe672-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe672-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

