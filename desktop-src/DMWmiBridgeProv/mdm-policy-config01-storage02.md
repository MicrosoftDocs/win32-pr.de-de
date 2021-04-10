---
title: MDM_Policy_Config01_Storage02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Storage02-Klasse konfiguriert die Speicher Richtlinien.
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- MDM_Policy_Config01_Storage02-Klasse
- MDM_Policy_Config01_Storage02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103893"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="563c3-105">MDM- \_ Richtlinie \_ Config01 \_ Storage02-Klasse</span><span class="sxs-lookup"><span data-stu-id="563c3-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="563c3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="563c3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="563c3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="563c3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="563c3-108">Die MDM- \_ Richtlinie \_ Config01 \_ Storage02-Klasse konfiguriert die Speicher Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="563c3-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="563c3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="563c3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="563c3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="563c3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="563c3-111">Member</span><span class="sxs-lookup"><span data-stu-id="563c3-111">Members</span></span>

<span data-ttu-id="563c3-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Storage02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="563c3-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="563c3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="563c3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="563c3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="563c3-114">Properties</span></span>

<span data-ttu-id="563c3-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Storage02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="563c3-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="563c3-116">Allowdiskhealthmodelupdates</span><span class="sxs-lookup"><span data-stu-id="563c3-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="563c3-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="563c3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="563c3-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="563c3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="563c3-119">Enhancedstoragedevices</span><span class="sxs-lookup"><span data-stu-id="563c3-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="563c3-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="563c3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="563c3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="563c3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="563c3-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="563c3-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="563c3-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="563c3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="563c3-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="563c3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="563c3-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="563c3-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="563c3-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="563c3-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="563c3-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="563c3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="563c3-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="563c3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="563c3-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="563c3-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="563c3-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="563c3-130">Requirements</span></span>



| <span data-ttu-id="563c3-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="563c3-131">Requirement</span></span> | <span data-ttu-id="563c3-132">Wert</span><span class="sxs-lookup"><span data-stu-id="563c3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="563c3-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="563c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="563c3-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="563c3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="563c3-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="563c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="563c3-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="563c3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="563c3-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="563c3-137">Namespace</span></span><br/>                | <span data-ttu-id="563c3-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="563c3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="563c3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="563c3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="563c3-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="563c3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="563c3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="563c3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="563c3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="563c3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

