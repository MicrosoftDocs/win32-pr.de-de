---
title: MDM_Policy_Result01_Maps02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Maps02-Klasse stellt die verfügbaren Zuordnungs Richtlinien dar.
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- MDM_Policy_Result01_Maps02-Klasse
- MDM_Policy_Result01_Maps02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476269"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="02036-105">MDM- \_ Richtlinie \_ Result01 \_ Maps02-Klasse</span><span class="sxs-lookup"><span data-stu-id="02036-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="02036-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="02036-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="02036-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="02036-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="02036-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Maps02** -Klasse stellt die verfügbaren Zuordnungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="02036-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="02036-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="02036-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="02036-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="02036-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="02036-111">Member</span><span class="sxs-lookup"><span data-stu-id="02036-111">Members</span></span>

<span data-ttu-id="02036-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Maps02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02036-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="02036-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02036-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02036-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02036-114">Properties</span></span>

<span data-ttu-id="02036-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Maps02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02036-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="02036-116">Allowofflinemapsdownloadovermeteredconnection</span><span class="sxs-lookup"><span data-stu-id="02036-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02036-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02036-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02036-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02036-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="02036-119">Enableofflinemapsautoupdate</span><span class="sxs-lookup"><span data-stu-id="02036-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="02036-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="02036-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="02036-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02036-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="02036-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="02036-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02036-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="02036-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02036-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02036-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02036-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02036-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02036-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="02036-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="02036-127">Für diese Klasse ist die Zeichenfolge "Maps".</span><span class="sxs-lookup"><span data-stu-id="02036-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="02036-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="02036-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02036-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="02036-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02036-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02036-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02036-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02036-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02036-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="02036-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="02036-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="02036-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02036-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02036-134">Requirements</span></span>



| <span data-ttu-id="02036-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02036-135">Requirement</span></span> | <span data-ttu-id="02036-136">Wert</span><span class="sxs-lookup"><span data-stu-id="02036-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02036-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02036-137">Minimum supported client</span></span><br/> | <span data-ttu-id="02036-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02036-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="02036-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02036-139">Minimum supported server</span></span><br/> | <span data-ttu-id="02036-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="02036-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="02036-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="02036-141">Namespace</span></span><br/>                | <span data-ttu-id="02036-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="02036-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="02036-143">MOF</span><span class="sxs-lookup"><span data-stu-id="02036-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02036-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02036-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="02036-145">DLL</span><span class="sxs-lookup"><span data-stu-id="02036-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02036-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="02036-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

