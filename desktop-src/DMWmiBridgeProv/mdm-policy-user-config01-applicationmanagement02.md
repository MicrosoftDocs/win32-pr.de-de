---
title: MDM_Policy_User_Config01_ApplicationManagement02-Klasse
description: Die Benutzer Config01 ApplicationManagement02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Start Richtlinien dar, die pro Benutzer festgelegt werden.
ms.assetid: 3dd20364-6723-4ed6-87c0-729789ddd948
keywords:
- MDM_Policy_User_Config01_ApplicationManagement02-Klasse
- MDM_Policy_User_Config01_ApplicationManagement02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88226122eefb3335ef1b19680268ea5acf1d5388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102966"
---
# <a name="mdm_policy_user_config01_applicationmanagement02-class"></a><span data-ttu-id="486b1-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ ApplicationManagement02-Klasse</span><span class="sxs-lookup"><span data-stu-id="486b1-105">MDM\_Policy\_User\_Config01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="486b1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="486b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="486b1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="486b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="486b1-108">Die **\_ \_ Benutzer \_ Config01 \_ ApplicationManagement02-Klasse der MDM-Richtlinie** stellt die verfügbaren Start Richtlinien dar, die pro Benutzer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="486b1-108">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="486b1-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="486b1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="486b1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="486b1-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="486b1-111">Member</span><span class="sxs-lookup"><span data-stu-id="486b1-111">Members</span></span>

<span data-ttu-id="486b1-112">Die **\_ \_ Benutzer \_ Config01 \_ ApplicationManagement02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="486b1-112">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="486b1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="486b1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="486b1-114">Properties</span></span>

<span data-ttu-id="486b1-115">Die **\_ \_ Benutzer \_ Config01 \_ ApplicationManagement02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="486b1-115">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="486b1-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="486b1-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="486b1-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="486b1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="486b1-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="486b1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="486b1-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="486b1-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="486b1-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="486b1-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="486b1-121">Für diese Klasse ist die Zeichenfolge "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="486b1-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="486b1-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="486b1-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="486b1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="486b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="486b1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="486b1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="486b1-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="486b1-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="486b1-126">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="486b1-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="486b1-127">Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="486b1-127">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="486b1-128">Requirements privatestoreonly</span><span class="sxs-lookup"><span data-stu-id="486b1-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="486b1-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="486b1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="486b1-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="486b1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="486b1-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="486b1-131">Requirements</span></span>



| <span data-ttu-id="486b1-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="486b1-132">Requirement</span></span> | <span data-ttu-id="486b1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="486b1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="486b1-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="486b1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="486b1-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="486b1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="486b1-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="486b1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="486b1-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="486b1-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="486b1-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="486b1-138">Namespace</span></span><br/>                | <span data-ttu-id="486b1-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="486b1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="486b1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="486b1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="486b1-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="486b1-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="486b1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="486b1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="486b1-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="486b1-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="486b1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="486b1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="486b1-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="486b1-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

