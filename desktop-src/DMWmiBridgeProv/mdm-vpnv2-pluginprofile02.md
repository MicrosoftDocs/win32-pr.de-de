---
title: MDM_VPNv2_PluginProfile02-Klasse
description: Die MDM \_ VPNv2 \_ PlugInProfile02-Klasse beschreibt die Informationen, die bei Verwendung eines Windows Store-basierten VPN-Plug-Ins erforderlich sind.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- MDM_VPNv2_PluginProfile02-Klasse
- MDM_VPNv2_PluginProfile02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956479"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="2310d-105">MDM \_ VPNv2 \_ PluginProfile02-Klasse</span><span class="sxs-lookup"><span data-stu-id="2310d-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="2310d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2310d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2310d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2310d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2310d-108">Die **MDM \_ VPNv2 \_ PlugInProfile02** -Klasse beschreibt die Informationen, die bei Verwendung eines Windows Store-basierten VPN-Plug-Ins erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2310d-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="2310d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2310d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2310d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2310d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="2310d-111">Member</span><span class="sxs-lookup"><span data-stu-id="2310d-111">Members</span></span>

<span data-ttu-id="2310d-112">Die **MDM \_ VPNv2 \_ PluginProfile02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2310d-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="2310d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2310d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2310d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2310d-114">Properties</span></span>

<span data-ttu-id="2310d-115">Die **MDM \_ VPNv2 \_ PluginProfile02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2310d-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2310d-116">Customconfiguration</span><span class="sxs-lookup"><span data-stu-id="2310d-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2310d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2310d-119">Customstoreurl</span><span class="sxs-lookup"><span data-stu-id="2310d-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2310d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2310d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2310d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2310d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2310d-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2310d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2310d-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2310d-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="2310d-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2310d-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2310d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2310d-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2310d-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2310d-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2310d-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2310d-132">Für diese Klasse ist die Zeichen *Folge "./Vendor/MSFT/VPNv2/profile* Name".</span><span class="sxs-lookup"><span data-stu-id="2310d-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="2310d-133">Pluginpackagefamilyname</span><span class="sxs-lookup"><span data-stu-id="2310d-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2310d-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2310d-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="2310d-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2310d-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2310d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2310d-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2310d-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2310d-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2310d-139">Requirements</span></span>



| <span data-ttu-id="2310d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2310d-140">Requirement</span></span> | <span data-ttu-id="2310d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2310d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2310d-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2310d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2310d-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2310d-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2310d-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2310d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2310d-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2310d-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2310d-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="2310d-146">Namespace</span></span><br/>                | <span data-ttu-id="2310d-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2310d-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2310d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2310d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2310d-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2310d-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2310d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2310d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2310d-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2310d-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2310d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2310d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2310d-153">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2310d-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

