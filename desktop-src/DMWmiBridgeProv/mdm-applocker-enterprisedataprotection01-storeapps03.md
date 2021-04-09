---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse
description: Die MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse erfasst die Liste der Windows-apps, die zum Verarbeiten von Unternehmensdaten berechtigt sind. Sollte in Verbindung mit den Einstellungen in./Vendor/MSFT/Policy/configSource/DataProtection verwendet werden.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957145"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="6de93-106">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03-Klasse</span><span class="sxs-lookup"><span data-stu-id="6de93-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="6de93-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6de93-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6de93-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6de93-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6de93-109">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse erfasst die Liste der Windows-apps, die zum Verarbeiten von Unternehmensdaten berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="6de93-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="6de93-110">Sollte in Verbindung mit den Einstellungen in./Vendor/MSFT/Policy/configSource/DataProtection verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6de93-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="6de93-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6de93-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de93-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6de93-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="6de93-113">Member</span><span class="sxs-lookup"><span data-stu-id="6de93-113">Members</span></span>

<span data-ttu-id="6de93-114">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6de93-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="6de93-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de93-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6de93-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de93-116">Properties</span></span>

<span data-ttu-id="6de93-117">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6de93-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6de93-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6de93-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de93-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de93-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de93-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de93-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de93-121">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6de93-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6de93-122">Legt Beschränkungen zum Ausführen von Apps vom Windows Store fest.</span><span class="sxs-lookup"><span data-stu-id="6de93-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="6de93-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6de93-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de93-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de93-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de93-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de93-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de93-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6de93-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6de93-127">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="6de93-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="6de93-128">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Gruppierung*".</span><span class="sxs-lookup"><span data-stu-id="6de93-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="6de93-129">**Policy**</span><span class="sxs-lookup"><span data-stu-id="6de93-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de93-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de93-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de93-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6de93-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6de93-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de93-132">Requirements</span></span>



| <span data-ttu-id="6de93-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de93-133">Requirement</span></span> | <span data-ttu-id="6de93-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6de93-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de93-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6de93-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6de93-136">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6de93-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6de93-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6de93-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6de93-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6de93-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6de93-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="6de93-139">Namespace</span></span><br/>                | <span data-ttu-id="6de93-140">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6de93-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6de93-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6de93-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6de93-142"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6de93-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6de93-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6de93-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de93-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de93-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de93-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6de93-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de93-146">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="6de93-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

