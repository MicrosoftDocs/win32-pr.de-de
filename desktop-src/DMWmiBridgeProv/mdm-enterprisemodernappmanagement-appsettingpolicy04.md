---
title: MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse
description: Die MDM \_ enterprismodernappmanagement \_ AppSettingPolicy04-Klasse gibt alle Werte für verwaltete App-Einstellungen an.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040832"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="016f0-105">MDM \_ enterprismodernappmanagement \_ AppSettingPolicy04-Klasse</span><span class="sxs-lookup"><span data-stu-id="016f0-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="016f0-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="016f0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="016f0-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="016f0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="016f0-108">Die **MDM \_ enterprismodernappmanagement \_ AppSettingPolicy04** -Klasse gibt alle Werte für verwaltete App-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="016f0-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="016f0-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="016f0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="016f0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="016f0-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="016f0-111">Member</span><span class="sxs-lookup"><span data-stu-id="016f0-111">Members</span></span>

<span data-ttu-id="016f0-112">Die **MDM \_ enterpritarmodernappmanagement \_ AppSettingPolicy04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="016f0-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="016f0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="016f0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="016f0-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="016f0-114">Properties</span></span>

<span data-ttu-id="016f0-115">Die **MDM \_ enterprismodernappmanagement \_ AppSettingPolicy04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="016f0-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="016f0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="016f0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="016f0-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="016f0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="016f0-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="016f0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="016f0-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="016f0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="016f0-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="016f0-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="016f0-121">Für diese Klasse die Zeichenfolge "appsettingpolicy".</span><span class="sxs-lookup"><span data-stu-id="016f0-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="016f0-122">Isvariableleaf</span><span class="sxs-lookup"><span data-stu-id="016f0-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="016f0-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="016f0-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="016f0-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="016f0-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="016f0-125">Hinzugefügt in Windows 10, Version 1511.</span><span class="sxs-lookup"><span data-stu-id="016f0-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="016f0-126">Der **SettingValue** und die Daten stellen ein Schlüssel-Wert-Paar dar, das für die APP konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="016f0-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="016f0-127">Der Knoten stellt den Namen des Schlüssels dar, und die Daten repräsentieren den Wert.</span><span class="sxs-lookup"><span data-stu-id="016f0-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="016f0-128">Sie finden diesen Wert in LocalSettings im Container Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="016f0-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="016f0-129">Diese Einstellung funktioniert nur für apps, die diese Funktion unterstützen, und wird nur im Benutzer Kontext unterstützt.</span><span class="sxs-lookup"><span data-stu-id="016f0-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="016f0-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="016f0-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="016f0-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="016f0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="016f0-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="016f0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="016f0-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="016f0-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="016f0-134">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="016f0-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="016f0-135">Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*packagefamilyname*".</span><span class="sxs-lookup"><span data-stu-id="016f0-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="016f0-136">**Wert**</span><span class="sxs-lookup"><span data-stu-id="016f0-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="016f0-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="016f0-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="016f0-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="016f0-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="016f0-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="016f0-139">Requirements</span></span>



| <span data-ttu-id="016f0-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="016f0-140">Requirement</span></span> | <span data-ttu-id="016f0-141">Wert</span><span class="sxs-lookup"><span data-stu-id="016f0-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="016f0-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="016f0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="016f0-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="016f0-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="016f0-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="016f0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="016f0-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="016f0-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="016f0-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="016f0-146">Namespace</span></span><br/>                | <span data-ttu-id="016f0-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="016f0-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="016f0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="016f0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="016f0-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="016f0-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="016f0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="016f0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="016f0-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016f0-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016f0-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="016f0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016f0-153">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="016f0-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

