---
title: MDM_AppLocker_EnterpriseDataProtection01_EXE03-Klasse
description: Die MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03-Klasse erfasst die Liste der ausführbaren Anwendungen, die zum Verarbeiten von Enterprise-Daten berechtigt sind.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03-Klasse
- MDM_AppLocker_EnterpriseDataProtection01_EXE03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106149"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="9ccda-105">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ccda-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="9ccda-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9ccda-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9ccda-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="9ccda-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9ccda-108">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** -Klasse erfasst die Liste der ausführbaren Anwendungen, die zum Verarbeiten von Enterprise-Daten berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="9ccda-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="9ccda-109">Sollte in Verbindung mit den Einstellungen in./Vendor/MSFT/Policy/configSource/DataProtection verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ccda-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="9ccda-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9ccda-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ccda-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ccda-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="9ccda-112">Member</span><span class="sxs-lookup"><span data-stu-id="9ccda-112">Members</span></span>

<span data-ttu-id="9ccda-113">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9ccda-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="9ccda-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ccda-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ccda-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9ccda-115">Properties</span></span>

<span data-ttu-id="9ccda-116">Die **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9ccda-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ccda-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9ccda-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccda-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ccda-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccda-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ccda-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccda-120">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ccda-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ccda-121">Definiert Einschränkungen für das Starten ausführbarer Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9ccda-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="9ccda-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9ccda-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccda-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ccda-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccda-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9ccda-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ccda-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ccda-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ccda-126">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="9ccda-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="9ccda-127">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Gruppierung*".</span><span class="sxs-lookup"><span data-stu-id="9ccda-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="9ccda-128">**Policy**</span><span class="sxs-lookup"><span data-stu-id="9ccda-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ccda-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9ccda-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ccda-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9ccda-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ccda-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ccda-131">Requirements</span></span>



| <span data-ttu-id="9ccda-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ccda-132">Requirement</span></span> | <span data-ttu-id="9ccda-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9ccda-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccda-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ccda-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9ccda-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ccda-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ccda-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ccda-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9ccda-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9ccda-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9ccda-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ccda-138">Namespace</span></span><br/>                | <span data-ttu-id="9ccda-139">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9ccda-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9ccda-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9ccda-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ccda-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ccda-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ccda-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9ccda-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ccda-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ccda-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccda-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ccda-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccda-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="9ccda-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

