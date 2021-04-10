---
title: MDM_DevDetail_Microsoft02-Klasse
description: Die MDM \_ DevDetail \_ Microsoft02-Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- MDM_DevDetail_Microsoft02-Klasse
- MDM_DevDetail_Microsoft02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956870"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="2bb06-105">MDM \_ DevDetail \_ Microsoft02-Klasse</span><span class="sxs-lookup"><span data-stu-id="2bb06-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="2bb06-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2bb06-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2bb06-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2bb06-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2bb06-108">Die **MDM \_ DevDetail \_ Microsoft02** -Klasse behandelt das-Verwaltungs Objekt, das gerätespezifische Parameter für den OMA DM-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2bb06-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="2bb06-109">Diese Geräteparameter werden nicht automatisch vom Client an den Server gesendet, Sie können jedoch mithilfe von OMA DM-Befehlen von Servern abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="2bb06-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="2bb06-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2bb06-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb06-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb06-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="2bb06-112">Member</span><span class="sxs-lookup"><span data-stu-id="2bb06-112">Members</span></span>

<span data-ttu-id="2bb06-113">Die **MDM \_ DevDetail \_ Microsoft02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2bb06-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="2bb06-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bb06-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bb06-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bb06-115">Properties</span></span>

<span data-ttu-id="2bb06-116">Die **MDM \_ DevDetail \_ Microsoft02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bb06-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2bb06-117">Commercializationoperator</span><span class="sxs-lookup"><span data-stu-id="2bb06-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bb06-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="2bb06-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb06-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2bb06-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb06-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bb06-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bb06-127">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2bb06-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="2bb06-128">Für diese Klasse ist die Zeichenfolge "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="2bb06-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="2bb06-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="2bb06-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bb06-132">MobileID</span><span class="sxs-lookup"><span data-stu-id="2bb06-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bb06-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="2bb06-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb06-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2bb06-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2bb06-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-141">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bb06-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bb06-142">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2bb06-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="2bb06-143">Für diese Klasse ist die Zeichenfolge "./DevDetail/ext".</span><span class="sxs-lookup"><span data-stu-id="2bb06-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="2bb06-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="2bb06-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-145">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2bb06-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bb06-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="2bb06-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-148">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2bb06-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bb06-150">Radioswv</span><span class="sxs-lookup"><span data-stu-id="2bb06-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2bb06-153">Gibt die Versionsnummer der Radio Stack-Software zurück.</span><span class="sxs-lookup"><span data-stu-id="2bb06-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="2bb06-154">Auflösung</span><span class="sxs-lookup"><span data-stu-id="2bb06-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb06-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2bb06-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb06-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2bb06-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bb06-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bb06-157">Requirements</span></span>



| <span data-ttu-id="2bb06-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bb06-158">Requirement</span></span> | <span data-ttu-id="2bb06-159">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb06-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb06-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bb06-160">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb06-161">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb06-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bb06-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bb06-162">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb06-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2bb06-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2bb06-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bb06-164">Namespace</span></span><br/>                | <span data-ttu-id="2bb06-165">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2bb06-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2bb06-166">MOF</span><span class="sxs-lookup"><span data-stu-id="2bb06-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bb06-167"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2bb06-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bb06-168">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb06-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb06-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb06-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb06-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bb06-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb06-171">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2bb06-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

