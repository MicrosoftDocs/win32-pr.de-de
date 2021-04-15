---
title: MDM_RemoteFind_Location01-Klasse
description: Die MDM \_ remotefind \_ Location01-Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01-Klasse
- MDM_RemoteFind_Location01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475288"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="90c3c-105">MDM \_ remotefind \_ Location01-Klasse</span><span class="sxs-lookup"><span data-stu-id="90c3c-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="90c3c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="90c3c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90c3c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="90c3c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90c3c-108">Die **MDM \_ remotefind \_ Location01** -Klasse ruft die Speicherort Informationen für ein bestimmtes Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="90c3c-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="90c3c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="90c3c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c3c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="90c3c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="90c3c-111">Member</span><span class="sxs-lookup"><span data-stu-id="90c3c-111">Members</span></span>

<span data-ttu-id="90c3c-112">Die **MDM \_ remotefind \_ Location01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="90c3c-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="90c3c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90c3c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90c3c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90c3c-114">Properties</span></span>

<span data-ttu-id="90c3c-115">Die **MDM \_ remotefind \_ Location01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90c3c-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="90c3c-116">Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="90c3c-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="90c3c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90c3c-119">[Age](/windows/client-management/mdm/remotefind-csp#age) (Alter)</span><span class="sxs-lookup"><span data-stu-id="90c3c-119">[Age](/windows/client-management/mdm/remotefind-csp#age)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-120">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="90c3c-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90c3c-122">Höhe</span><span class="sxs-lookup"><span data-stu-id="90c3c-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-123">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="90c3c-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90c3c-125">Altitudäaccuracy</span><span class="sxs-lookup"><span data-stu-id="90c3c-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="90c3c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90c3c-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90c3c-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90c3c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90c3c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90c3c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90c3c-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="90c3c-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="90c3c-133">Für diese Klasse ist die Zeichenfolge "Location".</span><span class="sxs-lookup"><span data-stu-id="90c3c-133">For this class, the string is "Location".</span></span>

</dd> <dt>

<span data-ttu-id="90c3c-134">[Latitude](/windows/client-management/mdm/remotefind-csp#latitude) (Breitengrad)</span><span class="sxs-lookup"><span data-stu-id="90c3c-134">[Latitude](/windows/client-management/mdm/remotefind-csp#latitude)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-135">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="90c3c-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90c3c-137">[Longitude](/windows/client-management/mdm/remotefind-csp#longitude) (Längengrad)</span><span class="sxs-lookup"><span data-stu-id="90c3c-137">[Longitude](/windows/client-management/mdm/remotefind-csp#longitude)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-138">Datentyp: **real32**</span><span class="sxs-lookup"><span data-stu-id="90c3c-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90c3c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90c3c-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="90c3c-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c3c-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90c3c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90c3c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c3c-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90c3c-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90c3c-144">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="90c3c-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="90c3c-145">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/RemoteFind".</span><span class="sxs-lookup"><span data-stu-id="90c3c-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90c3c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90c3c-146">Requirements</span></span>



| <span data-ttu-id="90c3c-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90c3c-147">Requirement</span></span> | <span data-ttu-id="90c3c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="90c3c-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c3c-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90c3c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="90c3c-150">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90c3c-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90c3c-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90c3c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="90c3c-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90c3c-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="90c3c-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="90c3c-153">Namespace</span></span><br/>                | <span data-ttu-id="90c3c-154">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="90c3c-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="90c3c-155">MOF</span><span class="sxs-lookup"><span data-stu-id="90c3c-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90c3c-156"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90c3c-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="90c3c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="90c3c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c3c-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c3c-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="90c3c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90c3c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c3c-160">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="90c3c-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

