---
title: MDM_Policy_Result01_Messaging02-Klasse
description: Die MDM \_ -Richtlinie \_ Result01 \_ Messaging02-Klasse stellt die SMS-Sicherungs-und-Wiederherstellungs-und-Messaging überall dar.
ms.assetid: cdc92999-3a2b-4653-b64f-79e19abe5559
keywords:
- MDM_Policy_Result01_Messaging02-Klasse
- MDM_Policy_Result01_Messaging02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Messaging02
- MDM_Policy_Result01_Messaging02.InstanceID
- MDM_Policy_Result01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd0eda84b9e2492243b2af85457450b0e443a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949763"
---
# <a name="mdm_policy_result01_messaging02-class"></a><span data-ttu-id="00c77-105">MDM- \_ Richtlinie \_ Result01 \_ Messaging02-Klasse</span><span class="sxs-lookup"><span data-stu-id="00c77-105">MDM\_Policy\_Result01\_Messaging02 class</span></span>

<span data-ttu-id="00c77-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="00c77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="00c77-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="00c77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="00c77-108">Die MDM \_ -Richtlinie \_ Result01 \_ Messaging02-Klasse stellt die SMS-Sicherungs-und-Wiederherstellungs-und-Messaging überall dar.</span><span class="sxs-lookup"><span data-stu-id="00c77-108">The MDM\_Policy\_Result01\_Messaging02 class represents the text message back up and restore and Messaging Everywhere.</span></span>

<span data-ttu-id="00c77-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="00c77-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c77-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="00c77-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="00c77-111">Member</span><span class="sxs-lookup"><span data-stu-id="00c77-111">Members</span></span>

<span data-ttu-id="00c77-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Messaging02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="00c77-112">The **MDM\_Policy\_Result01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="00c77-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00c77-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00c77-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00c77-114">Properties</span></span>

<span data-ttu-id="00c77-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Messaging02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="00c77-115">The **MDM\_Policy\_Result01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="00c77-116">Allowmessagesync</span><span class="sxs-lookup"><span data-stu-id="00c77-116">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c77-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="00c77-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c77-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="00c77-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00c77-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="00c77-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c77-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="00c77-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c77-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00c77-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c77-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00c77-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00c77-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="00c77-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c77-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="00c77-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c77-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="00c77-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c77-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00c77-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00c77-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00c77-127">Requirements</span></span>



| <span data-ttu-id="00c77-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00c77-128">Requirement</span></span> | <span data-ttu-id="00c77-129">Wert</span><span class="sxs-lookup"><span data-stu-id="00c77-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c77-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00c77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00c77-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00c77-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00c77-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00c77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00c77-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00c77-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="00c77-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="00c77-134">Namespace</span></span><br/>                | <span data-ttu-id="00c77-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="00c77-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="00c77-136">MOF</span><span class="sxs-lookup"><span data-stu-id="00c77-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00c77-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="00c77-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="00c77-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00c77-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c77-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c77-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

