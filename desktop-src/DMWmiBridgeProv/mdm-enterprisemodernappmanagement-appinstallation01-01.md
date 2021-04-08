---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse
description: Die MDM \_ enterpritsmodernappmanagement \_ AppInstallation01 \_ 01-Klasse wird verwendet, um Apps aus dem Windows Store oder einem gehosteten Speicherort zu installieren.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse
- MDM_EnterpriseModernAppManagement_AppInstallation01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956864"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="3c41d-105">MDM \_ enterprismodernappmanagement \_ AppInstallation01 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="3c41d-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="3c41d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="3c41d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c41d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="3c41d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3c41d-108">Die **MDM \_ enterpritsmodernappmanagement \_ AppInstallation01 \_ 01** -Klasse wird verwendet, um Apps aus dem Windows Store oder einem gehosteten Speicherort zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3c41d-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="3c41d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="3c41d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c41d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c41d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="3c41d-111">Member</span><span class="sxs-lookup"><span data-stu-id="3c41d-111">Members</span></span>

<span data-ttu-id="3c41d-112">Die **MDM \_ enterpritarmodernappmanagement \_ AppInstallation01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c41d-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3c41d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="3c41d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c41d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c41d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c41d-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="3c41d-115">Methods</span></span>

<span data-ttu-id="3c41d-116">Die **MDM \_ enterprismodernappmanagement \_ AppInstallation01 \_ 01** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3c41d-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="3c41d-117">Methode</span><span class="sxs-lookup"><span data-stu-id="3c41d-117">Method</span></span>                                                                                                    | <span data-ttu-id="3c41d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c41d-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c41d-119">**"Hustedinstallmethod"**</span><span class="sxs-lookup"><span data-stu-id="3c41d-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="3c41d-120">Methode zum Ausführen einer Installation eines App-Pakets von einem gehosteten Speicherort aus (hierbei kann es sich um ein lokales Laufwerk, eine UNC-oder eine HTTPS-Datenquelle handeln).</span><span class="sxs-lookup"><span data-stu-id="3c41d-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="3c41d-121">**Storeingestallmethod**</span><span class="sxs-lookup"><span data-stu-id="3c41d-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="3c41d-122">Methode zum Ausführen einer App-Installation und einer Lizenz aus dem Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3c41d-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="3c41d-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c41d-123">Properties</span></span>

<span data-ttu-id="3c41d-124">Die **MDM \_ enterprismodernappmanagement \_ AppInstallation01 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c41d-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c41d-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c41d-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c41d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c41d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c41d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c41d-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="3c41d-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="3c41d-130">Für diese Klasse ist die Zeichenfolge "appinstallation".</span><span class="sxs-lookup"><span data-stu-id="3c41d-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="3c41d-131">LastError</span><span class="sxs-lookup"><span data-stu-id="3c41d-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c41d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3c41d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c41d-134">Lasterrorde SC</span><span class="sxs-lookup"><span data-stu-id="3c41d-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c41d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3c41d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c41d-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3c41d-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c41d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c41d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c41d-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c41d-141">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="3c41d-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="3c41d-142">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation".</span><span class="sxs-lookup"><span data-stu-id="3c41d-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="3c41d-143">Progressstatus</span><span class="sxs-lookup"><span data-stu-id="3c41d-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c41d-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3c41d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c41d-146">Status</span><span class="sxs-lookup"><span data-stu-id="3c41d-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c41d-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c41d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c41d-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3c41d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c41d-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c41d-149">Requirements</span></span>



| <span data-ttu-id="3c41d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c41d-150">Requirement</span></span> | <span data-ttu-id="3c41d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="3c41d-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c41d-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c41d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3c41d-153">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c41d-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c41d-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c41d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3c41d-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3c41d-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3c41d-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c41d-156">Namespace</span></span><br/>                | <span data-ttu-id="3c41d-157">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3c41d-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3c41d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3c41d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c41d-159"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c41d-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c41d-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3c41d-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c41d-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c41d-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c41d-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c41d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c41d-163">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="3c41d-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

