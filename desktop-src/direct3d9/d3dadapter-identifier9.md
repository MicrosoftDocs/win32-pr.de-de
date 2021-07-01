---
description: Enthält Informationen zum Identifizieren des Adapters.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9-Struktur (D3D9Types.h)
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
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129969"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="8c4e5-103">D3DADAPTER \_ IDENTIFIER9-Struktur</span><span class="sxs-lookup"><span data-stu-id="8c4e5-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="8c4e5-104">Enthält Informationen zum Identifizieren des Adapters.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c4e5-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="8c4e5-106">Member</span><span class="sxs-lookup"><span data-stu-id="8c4e5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c4e5-107">**Treiber**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-108">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-109">Wird für die Darstellung für den Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-109">Used for presentation to the user.</span></span> <span data-ttu-id="8c4e5-110">Dies sollte nicht verwendet werden, um bestimmte Treiber zu identifizieren, da viele verschiedene Zeichenfolgen demselben Gerät und Treiber von verschiedenen Anbietern zugeordnet sein können.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-112">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-113">Wird für die Darstellung für den Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-114">**Devicename**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-115">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-116">Gerätename für GDI.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-118">Typ: **[ **LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-119">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="8c4e5-120">Es ist gesetzlich, für den 64-Bit-Ganzzahlwert mit Vorzeichen weniger als und größer als Vergleiche zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="8c4e5-121">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="8c4e5-122">Verwenden Sie stattdessen DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="8c4e5-123">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-126">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="8c4e5-127">Es ist gesetzlich, < und > ganzzahligen 64-Bit-Wert mit Vorzeichen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="8c4e5-128">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="8c4e5-129">Verwenden Sie stattdessen DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="8c4e5-130">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-133">Identifizieren Sie die Version des Direct3D-Treibers.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="8c4e5-134">Es ist gesetzlich, < und > ganzzahligen 64-Bit-Wert mit Vorzeichen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="8c4e5-135">Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="8c4e5-136">Verwenden Sie stattdessen DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="8c4e5-137">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-138">**Vendorid**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-139">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-140">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="8c4e5-141">Fragen Sie diesen Member ab, um den Hersteller zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="8c4e5-142">Der Wert kann 0 (null) sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-144">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-145">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="8c4e5-146">Fragen Sie diesen Member ab, um den Typ des Chipsets zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="8c4e5-147">Der Wert kann 0 (null) sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-149">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-150">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="8c4e5-151">Fragen Sie dieses Member ab, um das Subsystem zu identifizieren, in der Regel das bestimmte Board.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="8c4e5-152">Der Wert kann 0 (null) sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-153">**Revision**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-154">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-155">Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="8c4e5-156">Fragen Sie diesen Member ab, um die Revisionsebene des Chipsets zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="8c4e5-157">Der Wert kann 0 (null) sein, wenn er unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-159">Typ: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-160">Kann abgefragt werden, um Änderungen im Treiber- und Chipsatz zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="8c4e5-161">Diese GUID ist ein eindeutiger Bezeichner für das Treiber- und Chipsatzpaar.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="8c4e5-162">Fragen Sie diesen Member ab, um Änderungen am Treiber und Chipsatz nachverfolgungen, um ein neues Profil für das Grafiksubsystem zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="8c4e5-163">DeviceIdentifier kann auch verwendet werden, um bestimmte problematische Treiber zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="8c4e5-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="8c4e5-165">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c4e5-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c4e5-166">Wird verwendet, um die Windows Hardware Quality Labs (WHQL) für dieses Treiber- und Gerätepaar zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="8c4e5-167">Das DWORD ist eine gepackte Datumsstruktur, die das Datum der Veröffentlichung des letzten vom Treiber bestandenen WHQL-Tests definiert.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="8c4e5-168">Es ist gesetzlich, vorgänge < und > für diesen Wert durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="8c4e5-169">Im Folgenden wird das Datumsformat veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="8c4e5-170">Bits</span><span class="sxs-lookup"><span data-stu-id="8c4e5-170">Bits</span></span>  |  <span data-ttu-id="8c4e5-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c4e5-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="8c4e5-172">31-16</span><span class="sxs-lookup"><span data-stu-id="8c4e5-172">31-16</span></span> | <span data-ttu-id="8c4e5-173">Das Jahr, eine Dezimalzahl von 1999 nach oben.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="8c4e5-174">15-8</span><span class="sxs-lookup"><span data-stu-id="8c4e5-174">15-8</span></span>  | <span data-ttu-id="8c4e5-175">Der Monat, eine Dezimalzahl von 1 bis 12.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="8c4e5-176">7-0</span><span class="sxs-lookup"><span data-stu-id="8c4e5-176">7-0</span></span>   | <span data-ttu-id="8c4e5-177">Der Tag, eine Dezimalzahl von 1 bis 31.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="8c4e5-178">Die folgenden Werte werden ebenfalls verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-178">The following values are also used.</span></span>



| <span data-ttu-id="8c4e5-179">Wert</span><span class="sxs-lookup"><span data-stu-id="8c4e5-179">Value</span></span>    |  <span data-ttu-id="8c4e5-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c4e5-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="8c4e5-181">0</span><span class="sxs-lookup"><span data-stu-id="8c4e5-181">0</span></span>   | <span data-ttu-id="8c4e5-182">Nicht zertifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-182">Not certified.</span></span>                                        |
| <span data-ttu-id="8c4e5-183">1</span><span class="sxs-lookup"><span data-stu-id="8c4e5-183">1</span></span>   | <span data-ttu-id="8c4e5-184">WHQL überprüft, aber es sind keine Datumsinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="8c4e5-185">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="8c4e5-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="8c4e5-186">Für Direct3D9Ex unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder mehr aktuelles Betriebssystem) gibt [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c4e5-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c4e5-187">Remarks</span></span>

<span data-ttu-id="8c4e5-188">Das folgende Pseudocodebeispiel veranschaulicht das Versionsformat, das in den Membern DriverVersion, DriverVersionLowPart und DriverVersionHighPart codiert ist.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="8c4e5-189">Weitere Informationen zum HIWORD-Makro, zum LOWORD-Makro und zur LARGE INTEGER-Struktur finden Sie im Platform \_ SDK.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="8c4e5-190">MAX \_ DEVICE IDENTIFIER STRING ist eine Konstante mit der folgenden \_ \_ Definition.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="8c4e5-191">Die Member VendorId, DeviceId, SubSysId und Revision können zusammen verwendet werden, um bestimmte Chipsätze zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="8c4e5-192">Verwenden Sie diese Member jedoch mit Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="8c4e5-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4e5-193">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8c4e5-193">Requirements</span></span>



| <span data-ttu-id="8c4e5-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c4e5-194">Requirement</span></span> | <span data-ttu-id="8c4e5-195">Wert</span><span class="sxs-lookup"><span data-stu-id="8c4e5-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4e5-196">Header</span><span class="sxs-lookup"><span data-stu-id="8c4e5-196">Header</span></span><br/> | <dl> <span data-ttu-id="8c4e5-197"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4e5-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4e5-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c4e5-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4e5-199">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8c4e5-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
