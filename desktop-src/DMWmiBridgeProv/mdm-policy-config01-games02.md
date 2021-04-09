---
title: MDM_Policy_Config01_Games02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Games02-Klasse konfiguriert die erweiterten Gaming-Dienste.
ms.assetid: 567cf1b0-9795-44d5-a002-a1c03a5bf45f
keywords:
- MDM_Policy_Config01_Games02-Klasse
- MDM_Policy_Config01_Games02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Games02
- MDM_Policy_Config01_Games02.InstanceID
- MDM_Policy_Config01_Games02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f1ea989133bfdbe9d63dbaacff899dd7464965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040914"
---
# <a name="mdm_policy_config01_games02-class"></a><span data-ttu-id="de823-105">MDM- \_ Richtlinie \_ Config01 \_ Games02-Klasse</span><span class="sxs-lookup"><span data-stu-id="de823-105">MDM\_Policy\_Config01\_Games02 class</span></span>

<span data-ttu-id="de823-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="de823-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de823-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="de823-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de823-108">Die MDM- \_ Richtlinie \_ Config01 \_ Games02-Klasse konfiguriert die erweiterten Gaming-Dienste.</span><span class="sxs-lookup"><span data-stu-id="de823-108">The MDM\_Policy\_Config01\_Games02 class configures the advanced gaming services.</span></span>

<span data-ttu-id="de823-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="de823-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de823-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="de823-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Games02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAdvancedGamingServices;
};
```

## <a name="members"></a><span data-ttu-id="de823-111">Member</span><span class="sxs-lookup"><span data-stu-id="de823-111">Members</span></span>

<span data-ttu-id="de823-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Games02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de823-112">The **MDM\_Policy\_Config01\_Games02** class has these types of members:</span></span>

-   [<span data-ttu-id="de823-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de823-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de823-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de823-114">Properties</span></span>

<span data-ttu-id="de823-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Games02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de823-115">The **MDM\_Policy\_Config01\_Games02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="de823-116">Allowadvancedgamingservices</span><span class="sxs-lookup"><span data-stu-id="de823-116">AllowAdvancedGamingServices</span></span>](/windows/client-management/mdm/policy-csp-games#games-allowadvancedgamingservices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de823-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="de823-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de823-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de823-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de823-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de823-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de823-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de823-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de823-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de823-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de823-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de823-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de823-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="de823-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de823-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de823-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de823-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de823-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de823-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de823-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de823-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de823-127">Requirements</span></span>



| <span data-ttu-id="de823-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de823-128">Requirement</span></span> | <span data-ttu-id="de823-129">Wert</span><span class="sxs-lookup"><span data-stu-id="de823-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de823-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de823-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de823-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de823-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de823-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de823-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de823-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="de823-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de823-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="de823-134">Namespace</span></span><br/>                | <span data-ttu-id="de823-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="de823-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="de823-136">MOF</span><span class="sxs-lookup"><span data-stu-id="de823-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de823-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de823-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de823-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de823-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de823-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de823-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

