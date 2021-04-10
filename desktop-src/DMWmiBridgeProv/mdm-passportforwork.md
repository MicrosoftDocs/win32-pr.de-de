---
title: MDM_PassportForWork-Klasse
description: MDM \_ passportforwork wird zur Bereitstellung von Windows Hello for Business verwendet.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- MDM_PassportForWork-Klasse
- MDM_PassportForWork-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040423"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="603c5-105">MDM \_ passportforwork-Klasse</span><span class="sxs-lookup"><span data-stu-id="603c5-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="603c5-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="603c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="603c5-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="603c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="603c5-108">**MDM \_ passportforwork** wird zur Bereitstellung von Windows Hello for Business verwendet.</span><span class="sxs-lookup"><span data-stu-id="603c5-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="603c5-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="603c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="603c5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="603c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="603c5-111">Member</span><span class="sxs-lookup"><span data-stu-id="603c5-111">Members</span></span>

<span data-ttu-id="603c5-112">Die **MDM \_ passportforwork** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="603c5-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="603c5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="603c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="603c5-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="603c5-114">Properties</span></span>

<span data-ttu-id="603c5-115">Die **MDM \_ passportforwork** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="603c5-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="603c5-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="603c5-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603c5-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="603c5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603c5-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="603c5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603c5-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="603c5-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="603c5-120">Gibt die Mandanten-ID im Format eines global eindeutigen Bezeichners (GUID) ohne geschweifte Klammern ({,}) an, die als Teil der Windows Hello for Business-Bereitstellung und-Verwaltung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="603c5-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="603c5-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="603c5-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603c5-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="603c5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603c5-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="603c5-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603c5-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="603c5-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="603c5-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="603c5-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="603c5-126">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/PassPortForWork/".</span><span class="sxs-lookup"><span data-stu-id="603c5-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="603c5-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="603c5-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="603c5-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="603c5-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="603c5-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="603c5-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="603c5-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="603c5-130">Requirements</span></span>



| <span data-ttu-id="603c5-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="603c5-131">Requirement</span></span> | <span data-ttu-id="603c5-132">Wert</span><span class="sxs-lookup"><span data-stu-id="603c5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603c5-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="603c5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="603c5-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="603c5-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="603c5-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="603c5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="603c5-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="603c5-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="603c5-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="603c5-137">Namespace</span></span><br/>                | <span data-ttu-id="603c5-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="603c5-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="603c5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="603c5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="603c5-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="603c5-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="603c5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="603c5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="603c5-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="603c5-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603c5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="603c5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603c5-144">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="603c5-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

