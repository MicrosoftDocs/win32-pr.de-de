---
title: MDM_PassportForWork_Policies02-Klasse
description: Die MDM \_ passportforwork \_ Policies02-Klasse stellt Windows Hello for Business bereit.
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- MDM_PassportForWork_Policies02-Klasse
- MDM_PassportForWork_Policies02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949684"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="90882-105">MDM \_ passportforwork \_ Policies02-Klasse</span><span class="sxs-lookup"><span data-stu-id="90882-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="90882-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="90882-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90882-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="90882-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90882-108">Die **MDM \_ passportforwork \_ Policies02** -Klasse stellt Windows Hello for Business bereit.</span><span class="sxs-lookup"><span data-stu-id="90882-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="90882-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="90882-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90882-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="90882-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="90882-111">Member</span><span class="sxs-lookup"><span data-stu-id="90882-111">Members</span></span>

<span data-ttu-id="90882-112">Die **MDM \_ passportforwork \_ Policies02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="90882-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="90882-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90882-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90882-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90882-114">Properties</span></span>

<span data-ttu-id="90882-115">Die **MDM \_ passportforwork \_ Policies02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90882-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90882-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90882-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90882-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90882-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90882-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90882-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90882-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90882-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90882-120">Der Stamm Knoten für Windows Hello for Business-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="90882-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="90882-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="90882-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90882-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90882-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90882-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90882-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90882-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90882-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90882-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="90882-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="90882-126">Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/PassPortForWork/*tenantid*".</span><span class="sxs-lookup"><span data-stu-id="90882-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="90882-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="90882-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90882-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="90882-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90882-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90882-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90882-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="90882-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90882-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="90882-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90882-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90882-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90882-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90882-133">Requirements</span></span>



| <span data-ttu-id="90882-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90882-134">Requirement</span></span> | <span data-ttu-id="90882-135">Wert</span><span class="sxs-lookup"><span data-stu-id="90882-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90882-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90882-136">Minimum supported client</span></span><br/> | <span data-ttu-id="90882-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90882-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90882-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90882-138">Minimum supported server</span></span><br/> | <span data-ttu-id="90882-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90882-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="90882-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="90882-140">Namespace</span></span><br/>                | <span data-ttu-id="90882-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="90882-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="90882-142">MOF</span><span class="sxs-lookup"><span data-stu-id="90882-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90882-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90882-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90882-144">DLL</span><span class="sxs-lookup"><span data-stu-id="90882-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90882-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90882-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90882-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90882-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90882-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="90882-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

