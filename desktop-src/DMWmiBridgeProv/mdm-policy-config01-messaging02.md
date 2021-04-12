---
title: MDM_Policy_Config01_Messaging02-Klasse
description: Die Config01 Messaging02-Klasse der MDM \_ -Richtlinie \_ ermöglicht das \_ Sichern und Wiederherstellen von Textnachrichten und das Messaging überall. Diese Richtlinie ermöglicht es einer Organisation, diese Funktionen zu deaktivieren, um zu verhindern, dass Informationen auf Servern außerhalb ihrer Kontrolle gespeichert werden.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- MDM_Policy_Config01_Messaging02-Klasse
- MDM_Policy_Config01_Messaging02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517735"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="1982f-106">MDM- \_ Richtlinie \_ Config01 \_ Messaging02-Klasse</span><span class="sxs-lookup"><span data-stu-id="1982f-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="1982f-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1982f-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1982f-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1982f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1982f-109">Die Config01 Messaging02-Klasse der MDM \_ -Richtlinie \_ ermöglicht das \_ Sichern und Wiederherstellen von Textnachrichten und das Messaging überall.</span><span class="sxs-lookup"><span data-stu-id="1982f-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="1982f-110">Diese Richtlinie ermöglicht es einer Organisation, diese Funktionen zu deaktivieren, um zu verhindern, dass Informationen auf Servern außerhalb ihrer Kontrolle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1982f-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="1982f-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1982f-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1982f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="1982f-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="1982f-113">Member</span><span class="sxs-lookup"><span data-stu-id="1982f-113">Members</span></span>

<span data-ttu-id="1982f-114">Die **MDM- \_ Richtlinie \_ Config01 \_ Messaging02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1982f-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="1982f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1982f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1982f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1982f-116">Properties</span></span>

<span data-ttu-id="1982f-117">Die **MDM- \_ Richtlinie \_ Config01 \_ Messaging02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1982f-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1982f-118">Allowmessagesync</span><span class="sxs-lookup"><span data-stu-id="1982f-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1982f-119">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1982f-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1982f-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1982f-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1982f-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1982f-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1982f-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1982f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1982f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1982f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1982f-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1982f-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1982f-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1982f-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1982f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1982f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1982f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1982f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1982f-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1982f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1982f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1982f-129">Requirements</span></span>



| <span data-ttu-id="1982f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1982f-130">Requirement</span></span> | <span data-ttu-id="1982f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1982f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1982f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1982f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1982f-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1982f-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1982f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1982f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1982f-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1982f-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1982f-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="1982f-136">Namespace</span></span><br/>                | <span data-ttu-id="1982f-137">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1982f-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1982f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1982f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1982f-139"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1982f-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1982f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1982f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1982f-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1982f-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

