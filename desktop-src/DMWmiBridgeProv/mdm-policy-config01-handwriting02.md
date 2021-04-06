---
title: MDM_Policy_Config01_Handwriting02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Handwriting02-Klasse wird verwendet, um den Standardmodus für das Handschrift Panel zu konfigurieren.
ms.assetid: 3b835b72-7985-45c9-afc4-b6fdc69b331b
keywords:
- MDM_Policy_Config01_Handwriting02-Klasse
- MDM_Policy_Config01_Handwriting02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Handwriting02
- MDM_Policy_Config01_Handwriting02.InstanceID
- MDM_Policy_Config01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef2aa5f8b6563126dfcdd9e75870334853db11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859191"
---
# <a name="mdm_policy_config01_handwriting02-class"></a><span data-ttu-id="8bf85-105">MDM- \_ Richtlinie \_ Config01 \_ Handwriting02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8bf85-105">MDM\_Policy\_Config01\_Handwriting02 class</span></span>

<span data-ttu-id="8bf85-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8bf85-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8bf85-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8bf85-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8bf85-108">Die MDM- \_ Richtlinie \_ Config01 \_ Handwriting02-Klasse wird verwendet, um den Standardmodus für das Handschrift Panel zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8bf85-108">The MDM\_Policy\_Config01\_Handwriting02 class is used to configure the default mode for the handwriting panel.</span></span>

<span data-ttu-id="8bf85-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8bf85-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf85-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bf85-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="8bf85-111">Member</span><span class="sxs-lookup"><span data-stu-id="8bf85-111">Members</span></span>

<span data-ttu-id="8bf85-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Handwriting02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8bf85-112">The **MDM\_Policy\_Config01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="8bf85-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bf85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bf85-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bf85-114">Properties</span></span>

<span data-ttu-id="8bf85-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Handwriting02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8bf85-115">The **MDM\_Policy\_Config01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bf85-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8bf85-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf85-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8bf85-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf85-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8bf85-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf85-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8bf85-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8bf85-120">Paneldefaultmodeangedockt</span><span class="sxs-lookup"><span data-stu-id="8bf85-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf85-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8bf85-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bf85-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8bf85-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8bf85-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8bf85-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf85-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8bf85-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf85-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8bf85-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf85-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8bf85-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bf85-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bf85-127">Requirements</span></span>



| <span data-ttu-id="8bf85-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bf85-128">Requirement</span></span> | <span data-ttu-id="8bf85-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8bf85-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf85-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bf85-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf85-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bf85-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bf85-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bf85-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf85-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8bf85-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8bf85-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bf85-134">Namespace</span></span><br/>                | <span data-ttu-id="8bf85-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8bf85-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8bf85-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf85-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf85-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8bf85-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf85-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf85-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf85-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bf85-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

