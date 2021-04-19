---
description: Enthält Informationen, die den Adapter identifizieren.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350670"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="f7eac-103">D3DADAPTER \_ IDENTIFIER9-Struktur</span><span class="sxs-lookup"><span data-stu-id="f7eac-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="f7eac-104">Enthält Informationen, die den Adapter identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7eac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7eac-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="f7eac-106">Member</span><span class="sxs-lookup"><span data-stu-id="f7eac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7eac-107">**Treiber**</span><span class="sxs-lookup"><span data-stu-id="f7eac-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-108">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="f7eac-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-109">Wird für die Darstellung an den Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7eac-109">Used for presentation to the user.</span></span> <span data-ttu-id="f7eac-110">Dies sollte nicht verwendet werden, um bestimmte Treiber zu identifizieren, da viele verschiedene Zeichen folgen mit demselben Gerät und Treiber von unterschiedlichen Anbietern verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="f7eac-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7eac-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-112">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="f7eac-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-113">Wird für die Darstellung an den Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7eac-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="f7eac-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-115">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="f7eac-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-116">Der Gerätename für GDI.</span><span class="sxs-lookup"><span data-stu-id="f7eac-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="f7eac-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-118">Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-119">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="f7eac-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f7eac-120">Es ist zulässig, kleiner als und größer als Vergleiche für den ganzzahligen Wert der 64-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f7eac-121">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f7eac-122">Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7eac-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f7eac-123">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f7eac-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-124">**Driverversionlowpart**</span><span class="sxs-lookup"><span data-stu-id="f7eac-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-126">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="f7eac-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f7eac-127">Es ist zulässig, < und > Vergleiche für den Wert der 64-Bit-Ganzzahl mit Vorzeichen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f7eac-128">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f7eac-129">Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7eac-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f7eac-130">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f7eac-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-131">**Driverversionhighpart**</span><span class="sxs-lookup"><span data-stu-id="f7eac-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-133">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="f7eac-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="f7eac-134">Es ist zulässig, < und > Vergleiche für den Wert der 64-Bit-Ganzzahl mit Vorzeichen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="f7eac-135">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="f7eac-136">Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7eac-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="f7eac-137">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f7eac-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-138">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="f7eac-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-139">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-140">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f7eac-141">Fragen Sie diesen Member ab, um den Hersteller zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="f7eac-142">Der Wert kann NULL sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7eac-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="f7eac-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-144">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-145">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f7eac-146">Fragen Sie diesen Member ab, um den Typ der Chipmenge zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="f7eac-147">Der Wert kann NULL sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7eac-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-148">**Subsysid**</span><span class="sxs-lookup"><span data-stu-id="f7eac-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-149">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-150">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f7eac-151">Fragen Sie dieses Element ab, um das Subsystem, normalerweise das jeweilige Board, zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="f7eac-152">Der Wert kann NULL sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7eac-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-153">**Novel**</span><span class="sxs-lookup"><span data-stu-id="f7eac-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-154">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-155">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="f7eac-156">Fragen Sie diesen Member ab, um die Revisions Ebene des Chipsatzes zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="f7eac-157">Der Wert kann NULL sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7eac-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-158">**Geräte Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="f7eac-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-159">Typ: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-160">Kann abgefragt werden, um die Änderungen im Treiber und Chip Satz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="f7eac-161">Diese GUID ist ein eindeutiger Bezeichner für das Treiber-und Chip Satz Paar.</span><span class="sxs-lookup"><span data-stu-id="f7eac-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="f7eac-162">Fragen Sie dieses Element ab, um Änderungen am Treiber und Chip Satz zu verfolgen, um ein neues Profil für das Grafik Subsystem zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="f7eac-163">Der Geräte Bezeichner kann auch verwendet werden, um bestimmte problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="f7eac-164">**Whqllevel**</span><span class="sxs-lookup"><span data-stu-id="f7eac-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="f7eac-165">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7eac-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f7eac-166">Dient zum Bestimmen der Windows Hardware Quality Labs (WHQL)-Validierungs Ebene für dieses Treiber-und Geräte Paar.</span><span class="sxs-lookup"><span data-stu-id="f7eac-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="f7eac-167">Das DWORD ist eine gepackte Datums Struktur, die das Datum der Freigabe des neuesten, vom Treiber übergebenen WHQL-Tests definiert.</span><span class="sxs-lookup"><span data-stu-id="f7eac-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="f7eac-168">Es ist zulässig, <-und > Vorgänge für diesen Wert auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="f7eac-169">Im folgenden wird das Datumsformat veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f7eac-169">The following illustrates the date format.</span></span>



|       |                                               |
|-------|-----------------------------------------------|
| <span data-ttu-id="f7eac-170">Bits</span><span class="sxs-lookup"><span data-stu-id="f7eac-170">Bits</span></span>  |                                               |
| <span data-ttu-id="f7eac-171">31-16</span><span class="sxs-lookup"><span data-stu-id="f7eac-171">31-16</span></span> | <span data-ttu-id="f7eac-172">Das Jahr, eine Dezimalzahl von 1999 aufwärts.</span><span class="sxs-lookup"><span data-stu-id="f7eac-172">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="f7eac-173">15-8</span><span class="sxs-lookup"><span data-stu-id="f7eac-173">15-8</span></span>  | <span data-ttu-id="f7eac-174">Der Monat, eine Dezimalzahl zwischen 1 und 12.</span><span class="sxs-lookup"><span data-stu-id="f7eac-174">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="f7eac-175">7-0</span><span class="sxs-lookup"><span data-stu-id="f7eac-175">7-0</span></span>   | <span data-ttu-id="f7eac-176">Der Tag, eine Dezimalzahl zwischen 1 und 31.</span><span class="sxs-lookup"><span data-stu-id="f7eac-176">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="f7eac-177">Die folgenden Werte werden ebenfalls verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7eac-177">The following values are also used.</span></span>



|     |                                                       |
|-----|-------------------------------------------------------|
| <span data-ttu-id="f7eac-178">0</span><span class="sxs-lookup"><span data-stu-id="f7eac-178">0</span></span>   | <span data-ttu-id="f7eac-179">Nicht zertifiziert.</span><span class="sxs-lookup"><span data-stu-id="f7eac-179">Not certified.</span></span>                                        |
| <span data-ttu-id="f7eac-180">1</span><span class="sxs-lookup"><span data-stu-id="f7eac-180">1</span></span>   | <span data-ttu-id="f7eac-181">WHQL wurde überprüft, aber es sind keine Datumsinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7eac-181">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="f7eac-182">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="f7eac-182">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="f7eac-183">Für Direct3D9Ex, die unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder höher) ausgeführt werden, gibt [**IDirect3D9:: getadapteridentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f7eac-183">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7eac-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7eac-184">Remarks</span></span>

<span data-ttu-id="f7eac-185">Im folgenden Pseudo Codebeispiel wird das Versions Format veranschaulicht, das in den Membern "DriverVersion", "driverversionlowpart" und "driverversionhighpart" codiert ist.</span><span class="sxs-lookup"><span data-stu-id="f7eac-185">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="f7eac-186">Weitere Informationen über das HIWORD-Makro, das LoWord-Makro und die große ganzzahlige Struktur finden Sie im Platform SDK \_ .</span><span class="sxs-lookup"><span data-stu-id="f7eac-186">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="f7eac-187">\_ \_ \_ Die Zeichenfolge für die maximale Gerätekennung ist eine Konstante mit der folgenden Definition.</span><span class="sxs-lookup"><span data-stu-id="f7eac-187">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="f7eac-188">Die Elemente VendorID, de viceid, subsysid und Revision können zusammen verwendet werden, um bestimmte Chip Sätze zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f7eac-188">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="f7eac-189">Verwenden Sie diese Member jedoch mit Bedacht.</span><span class="sxs-lookup"><span data-stu-id="f7eac-189">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7eac-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7eac-190">Requirements</span></span>



| <span data-ttu-id="f7eac-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7eac-191">Requirement</span></span> | <span data-ttu-id="f7eac-192">Wert</span><span class="sxs-lookup"><span data-stu-id="f7eac-192">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eac-193">Header</span><span class="sxs-lookup"><span data-stu-id="f7eac-193">Header</span></span><br/> | <dl> <span data-ttu-id="f7eac-194"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7eac-194"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7eac-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7eac-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7eac-196">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7eac-196">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
