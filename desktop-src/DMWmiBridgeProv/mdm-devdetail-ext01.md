---
title: MDM_DevDetail_Ext01-Klasse
description: Die MDM \_ DevDetail \_ Ext01-Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- MDM_DevDetail_Ext01-Klasse
- MDM_DevDetail_Ext01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742633"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="24c7e-105">MDM \_ DevDetail \_ Ext01-Klasse</span><span class="sxs-lookup"><span data-stu-id="24c7e-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="24c7e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="24c7e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="24c7e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="24c7e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="24c7e-108">Die **MDM \_ DevDetail \_ Ext01** -Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="24c7e-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="24c7e-109">Diese Geräteparameter werden nicht automatisch vom Client an den Server gesendet, Sie können jedoch mithilfe von OMA DM-Befehlen von Servern abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="24c7e-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="24c7e-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="24c7e-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c7e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="24c7e-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="24c7e-112">Member</span><span class="sxs-lookup"><span data-stu-id="24c7e-112">Members</span></span>

<span data-ttu-id="24c7e-113">Die **MDM \_ DevDetail \_ Ext01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="24c7e-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="24c7e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24c7e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24c7e-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24c7e-115">Properties</span></span>

<span data-ttu-id="24c7e-116">Die **MDM \_ DevDetail \_ Ext01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24c7e-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="24c7e-117">"Gerätedaten"</span><span class="sxs-lookup"><span data-stu-id="24c7e-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c7e-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c7e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c7e-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="24c7e-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="24c7e-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c7e-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c7e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c7e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24c7e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24c7e-124">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="24c7e-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="24c7e-125">Für diese Klasse ist die Zeichenfolge "ext".</span><span class="sxs-lookup"><span data-stu-id="24c7e-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="24c7e-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="24c7e-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c7e-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c7e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="24c7e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24c7e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24c7e-130">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="24c7e-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="24c7e-131">Für diese Klasse ist die Zeichenfolge "./DevDetail/".</span><span class="sxs-lookup"><span data-stu-id="24c7e-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="24c7e-132">Wlanmacaddress</span><span class="sxs-lookup"><span data-stu-id="24c7e-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24c7e-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="24c7e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24c7e-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="24c7e-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24c7e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24c7e-135">Requirements</span></span>



| <span data-ttu-id="24c7e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24c7e-136">Requirement</span></span> | <span data-ttu-id="24c7e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="24c7e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c7e-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24c7e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="24c7e-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24c7e-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24c7e-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24c7e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="24c7e-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24c7e-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="24c7e-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="24c7e-142">Namespace</span></span><br/>                | <span data-ttu-id="24c7e-143">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="24c7e-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="24c7e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="24c7e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24c7e-145"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24c7e-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="24c7e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="24c7e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24c7e-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24c7e-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c7e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24c7e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c7e-149">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="24c7e-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

