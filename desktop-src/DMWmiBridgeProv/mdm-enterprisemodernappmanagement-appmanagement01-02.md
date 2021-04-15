---
title: MDM_EnterpriseModernAppManagement_AppManagement01_02-Klasse
description: Die MDM \_ enterprigmodernappmanagement \_ AppManagement01 \_ 02-Klasse gibt an, ob eine bestimmte App über automatische Updates aktualisiert werden soll.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_02-Klasse
- MDM_EnterpriseModernAppManagement_AppManagement01_02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478060"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="a485f-105">MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 02-Klasse</span><span class="sxs-lookup"><span data-stu-id="a485f-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="a485f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a485f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a485f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a485f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a485f-108">Die **MDM \_ enterprigmodernappmanagement \_ AppManagement01 \_ 02** -Klasse gibt an, ob eine bestimmte App über automatische Updates aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a485f-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="a485f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a485f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a485f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a485f-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="a485f-111">Member</span><span class="sxs-lookup"><span data-stu-id="a485f-111">Members</span></span>

<span data-ttu-id="a485f-112">Die **MDM \_ enterpritarmodernappmanagement \_ AppManagement01 \_ 02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a485f-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="a485f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a485f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a485f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a485f-114">Properties</span></span>

<span data-ttu-id="a485f-115">Die **MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a485f-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a485f-116">Donotupdate</span><span class="sxs-lookup"><span data-stu-id="a485f-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a485f-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a485f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a485f-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a485f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a485f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a485f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a485f-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a485f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a485f-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a485f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a485f-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a485f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a485f-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="a485f-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="a485f-124">Bei dieser Klasse ist die Zeichenfolge die Instanz des Paket Familiennamens.</span><span class="sxs-lookup"><span data-stu-id="a485f-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="a485f-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a485f-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a485f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a485f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a485f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a485f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a485f-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a485f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a485f-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="a485f-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="a485f-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*enterpriseid*".</span><span class="sxs-lookup"><span data-stu-id="a485f-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a485f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a485f-131">Requirements</span></span>



| <span data-ttu-id="a485f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a485f-132">Requirement</span></span> | <span data-ttu-id="a485f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a485f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a485f-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a485f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a485f-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a485f-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a485f-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a485f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a485f-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a485f-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a485f-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a485f-138">Namespace</span></span><br/>                | <span data-ttu-id="a485f-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a485f-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a485f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a485f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a485f-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a485f-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a485f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a485f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a485f-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a485f-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a485f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a485f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a485f-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="a485f-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

