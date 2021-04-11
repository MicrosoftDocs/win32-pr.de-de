---
title: MDM_PassportForWork_ExcludeSecurityDevices03-Klasse
description: Die Klasse MDM \_ passportforwork \_ ExcludeSecurityDevices03 definiert die vertrauenswürdigen Plattformmodule, die mit Windows Hello for Business verwendet werden dürfen.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- MDM_PassportForWork_ExcludeSecurityDevices03-Klasse
- MDM_PassportForWork_ExcludeSecurityDevices03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040427"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="1ed59-105">MDM \_ passportforwork \_ ExcludeSecurityDevices03-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ed59-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="1ed59-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1ed59-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ed59-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="1ed59-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ed59-108">Die Klasse MDM \_ passportforwork \_ ExcludeSecurityDevices03 definiert die vertrauenswürdigen Plattformmodule, die mit Windows Hello for Business verwendet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="1ed59-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="1ed59-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1ed59-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed59-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed59-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="1ed59-111">Member</span><span class="sxs-lookup"><span data-stu-id="1ed59-111">Members</span></span>

<span data-ttu-id="1ed59-112">Die **MDM \_ passportforwork \_ ExcludeSecurityDevices03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ed59-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="1ed59-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ed59-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ed59-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ed59-114">Properties</span></span>

<span data-ttu-id="1ed59-115">Die **MDM \_ passportforwork \_ ExcludeSecurityDevices03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ed59-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ed59-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ed59-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ed59-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ed59-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ed59-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-120">Stammknoten.</span><span class="sxs-lookup"><span data-stu-id="1ed59-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="1ed59-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1ed59-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1ed59-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ed59-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ed59-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ed59-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="1ed59-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="1ed59-126">Weitere Informationen finden Sie unter [passportforwork CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="1ed59-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="1ed59-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="1ed59-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ed59-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1ed59-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ed59-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1ed59-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ed59-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ed59-130">Requirements</span></span>



| <span data-ttu-id="1ed59-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ed59-131">Requirement</span></span> | <span data-ttu-id="1ed59-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1ed59-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed59-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ed59-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed59-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ed59-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ed59-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ed59-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed59-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ed59-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1ed59-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ed59-137">Namespace</span></span><br/>                | <span data-ttu-id="1ed59-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1ed59-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1ed59-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1ed59-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ed59-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ed59-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ed59-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1ed59-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ed59-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ed59-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

