---
title: MDM_DevDetail-Klasse
description: Die MDM \_ DevDetail-Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- MDM_DevDetail-Klasse
- MDM_DevDetail-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345316"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="ae378-105">MDM \_ DevDetail-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae378-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="ae378-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ae378-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ae378-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ae378-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ae378-108">Die **MDM \_ DevDetail** -Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ae378-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="ae378-109">Diese Geräteparameter werden nicht automatisch vom Client an den Server gesendet, Sie können jedoch mithilfe von OMA DM-Befehlen von Servern abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ae378-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="ae378-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ae378-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae378-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae378-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="ae378-112">Member</span><span class="sxs-lookup"><span data-stu-id="ae378-112">Members</span></span>

<span data-ttu-id="ae378-113">Die **MDM \_ DevDetail** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ae378-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="ae378-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae378-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae378-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae378-115">Properties</span></span>

<span data-ttu-id="ae378-116">Die **MDM \_ DevDetail** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae378-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ae378-117">Devyp</span><span class="sxs-lookup"><span data-stu-id="ae378-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ae378-120">F-</span><span class="sxs-lookup"><span data-stu-id="ae378-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ae378-123">HWV</span><span class="sxs-lookup"><span data-stu-id="ae378-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae378-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae378-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae378-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae378-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae378-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae378-130">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ae378-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="ae378-131">Für diese Klasse lautet die Zeichenfolge "DevDetail".</span><span class="sxs-lookup"><span data-stu-id="ae378-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="ae378-132">Lrgobj</span><span class="sxs-lookup"><span data-stu-id="ae378-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ae378-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ae378-135">OEM</span><span class="sxs-lookup"><span data-stu-id="ae378-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae378-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ae378-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae378-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae378-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae378-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae378-142">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ae378-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="ae378-143">Austauschen</span><span class="sxs-lookup"><span data-stu-id="ae378-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae378-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae378-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae378-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ae378-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae378-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae378-146">Requirements</span></span>



| <span data-ttu-id="ae378-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae378-147">Requirement</span></span> | <span data-ttu-id="ae378-148">Wert</span><span class="sxs-lookup"><span data-stu-id="ae378-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae378-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae378-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ae378-150">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae378-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae378-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae378-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ae378-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ae378-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ae378-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae378-153">Namespace</span></span><br/>                | <span data-ttu-id="ae378-154">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ae378-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ae378-155">MOF</span><span class="sxs-lookup"><span data-stu-id="ae378-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae378-156"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae378-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae378-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ae378-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae378-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae378-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae378-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae378-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae378-160">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ae378-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

