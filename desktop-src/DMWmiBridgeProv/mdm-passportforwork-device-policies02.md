---
title: MDM_PassportForWork_Device_Policies02-Klasse
description: Die MDM \_ passportforwork- \_ Geräte \_ Policies02 Klasse definiert die Richtlinien Einstellungen für Windows Hello for Business.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- MDM_PassportForWork_Device_Policies02-Klasse
- MDM_PassportForWork_Device_Policies02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949687"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="45768-105">MDM \_ passportforwork- \_ Gerät \_ Policies02 Klasse</span><span class="sxs-lookup"><span data-stu-id="45768-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="45768-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="45768-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="45768-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="45768-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="45768-108">Die **MDM \_ passportforwork- \_ Geräte \_ Policies02** Klasse definiert die Richtlinien Einstellungen für Windows Hello for Business.</span><span class="sxs-lookup"><span data-stu-id="45768-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="45768-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="45768-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45768-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="45768-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="45768-111">Member</span><span class="sxs-lookup"><span data-stu-id="45768-111">Members</span></span>

<span data-ttu-id="45768-112">Die **MDM \_ passportforwork- \_ Geräte \_ Policies02** Klasse verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45768-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="45768-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45768-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45768-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45768-114">Properties</span></span>

<span data-ttu-id="45768-115">Die **MDM \_ passportforwork- \_ Geräte \_ Policies02** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45768-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45768-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="45768-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45768-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45768-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45768-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45768-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45768-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45768-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45768-120">Knoten für die Richtlinien Einstellungen für Windows Hello for Business.</span><span class="sxs-lookup"><span data-stu-id="45768-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="45768-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="45768-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45768-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="45768-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45768-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="45768-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45768-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45768-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45768-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="45768-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="45768-126">Für diese Klasse ist die Zeichenfolge "./Device/Vendor/MSFT/PassPortForWork/*tenantid*/".</span><span class="sxs-lookup"><span data-stu-id="45768-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="45768-127">Usecertificateforonpremauth</span><span class="sxs-lookup"><span data-stu-id="45768-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="45768-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="45768-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45768-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45768-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45768-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45768-130">Requirements</span></span>



| <span data-ttu-id="45768-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45768-131">Requirement</span></span> | <span data-ttu-id="45768-132">Wert</span><span class="sxs-lookup"><span data-stu-id="45768-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45768-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45768-133">Minimum supported client</span></span><br/> | <span data-ttu-id="45768-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45768-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45768-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45768-135">Minimum supported server</span></span><br/> | <span data-ttu-id="45768-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="45768-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="45768-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="45768-137">Namespace</span></span><br/>                | <span data-ttu-id="45768-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="45768-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="45768-139">MOF</span><span class="sxs-lookup"><span data-stu-id="45768-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45768-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="45768-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="45768-141">DLL</span><span class="sxs-lookup"><span data-stu-id="45768-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45768-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45768-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

