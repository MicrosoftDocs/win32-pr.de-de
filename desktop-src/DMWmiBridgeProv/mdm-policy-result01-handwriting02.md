---
title: MDM_Policy_Result01_Handwriting02-Klasse
description: Die Result01 Handwriting02-Klasse der MDM- \_ Richtlinie \_ \_ stellt den Standardmodus für das Handschrift Panel dar.
ms.assetid: b21d0208-210d-476f-9269-f8d8a3307f17
keywords:
- MDM_Policy_Result01_Handwriting02-Klasse
- MDM_Policy_Result01_Handwriting02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Handwriting02
- MDM_Policy_Result01_Handwriting02.InstanceID
- MDM_Policy_Result01_Handwriting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636dcfbb0d3bceaf60697d2aaa6e7f158a052bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104019"
---
# <a name="mdm_policy_result01_handwriting02-class"></a><span data-ttu-id="7a347-105">MDM- \_ Richtlinie \_ Result01 \_ Handwriting02-Klasse</span><span class="sxs-lookup"><span data-stu-id="7a347-105">MDM\_Policy\_Result01\_Handwriting02 class</span></span>

<span data-ttu-id="7a347-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7a347-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7a347-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7a347-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7a347-108">Die Result01 Handwriting02-Klasse der MDM- \_ Richtlinie \_ \_ stellt den Standardmodus für das Handschrift Panel dar.</span><span class="sxs-lookup"><span data-stu-id="7a347-108">The MDM\_Policy\_Result01\_Handwriting02 class represents the default mode for the handwriting panel.</span></span>

<span data-ttu-id="7a347-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7a347-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a347-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a347-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Handwriting02
{
  string InstanceID;
  string ParentID;
  sint32 PanelDefaultModeDocked;
};
```

## <a name="members"></a><span data-ttu-id="7a347-111">Member</span><span class="sxs-lookup"><span data-stu-id="7a347-111">Members</span></span>

<span data-ttu-id="7a347-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Handwriting02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7a347-112">The **MDM\_Policy\_Result01\_Handwriting02** class has these types of members:</span></span>

-   [<span data-ttu-id="7a347-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a347-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a347-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a347-114">Properties</span></span>

<span data-ttu-id="7a347-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Handwriting02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a347-115">The **MDM\_Policy\_Result01\_Handwriting02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a347-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7a347-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a347-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a347-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a347-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a347-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a347-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a347-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7a347-120">Paneldefaultmodeangedockt</span><span class="sxs-lookup"><span data-stu-id="7a347-120">PanelDefaultModeDocked</span></span>](/windows/client-management/mdm/policy-csp-handwriting#handwriting-paneldefaultmodedocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a347-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a347-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a347-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a347-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7a347-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7a347-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a347-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7a347-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a347-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7a347-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a347-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a347-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a347-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a347-127">Requirements</span></span>



| <span data-ttu-id="7a347-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a347-128">Requirement</span></span> | <span data-ttu-id="7a347-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7a347-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a347-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a347-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a347-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a347-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a347-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a347-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a347-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a347-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7a347-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a347-134">Namespace</span></span><br/>                | <span data-ttu-id="7a347-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7a347-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7a347-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7a347-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a347-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a347-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a347-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a347-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a347-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a347-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

