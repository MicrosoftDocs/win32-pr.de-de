---
title: DDS_PIXELFORMAT-Struktur (DDS. h)
description: Das Oberflächen Pixel Format.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354991"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="e9ebe-104">DDS- \_ Pixel Format-Struktur</span><span class="sxs-lookup"><span data-stu-id="e9ebe-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="e9ebe-105">Das Oberflächen Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ebe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9ebe-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="e9ebe-107">Member</span><span class="sxs-lookup"><span data-stu-id="e9ebe-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9ebe-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-109">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-110">Struktur Größe; auf 32 (Bytes) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-112">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-113">Werte, die angeben, welche Art von Daten auf der-Oberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="e9ebe-114">Flag</span><span class="sxs-lookup"><span data-stu-id="e9ebe-114">Flag</span></span>              | <span data-ttu-id="e9ebe-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9ebe-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="e9ebe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ebe-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="e9ebe-117">ddpf- \_ alphabepixel</span><span class="sxs-lookup"><span data-stu-id="e9ebe-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="e9ebe-118">Textur enthält Alpha Daten; **dwrgbalphabitmask** enthält gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="e9ebe-119">0x1</span><span class="sxs-lookup"><span data-stu-id="e9ebe-119">0x1</span></span>     |
| <span data-ttu-id="e9ebe-120">ddpf- \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="e9ebe-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="e9ebe-121">Wird in einigen älteren DDS-Dateien für nicht komprimierte Alphakanäle-Daten verwendet (dwrgbbitcount enthält den Alphakanal bitCount; dwabitmask enthält gültige Daten)</span><span class="sxs-lookup"><span data-stu-id="e9ebe-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="e9ebe-122">0x2</span><span class="sxs-lookup"><span data-stu-id="e9ebe-122">0x2</span></span>     |
| <span data-ttu-id="e9ebe-123">ddpf \_ FourCC</span><span class="sxs-lookup"><span data-stu-id="e9ebe-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="e9ebe-124">Textur enthält komprimierte RGB-Daten. **dwfourcc** enthält gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="e9ebe-125">0x4</span><span class="sxs-lookup"><span data-stu-id="e9ebe-125">0x4</span></span>     |
| <span data-ttu-id="e9ebe-126">ddpf- \_ RGB</span><span class="sxs-lookup"><span data-stu-id="e9ebe-126">DDPF\_RGB</span></span>         | <span data-ttu-id="e9ebe-127">Textur enthält unkomprimierte RGB-Daten. die **dwrgbbitcount** -und RGB-Masken (**dwrbitmask**, **dwgbitmask**, **dwbbitmask**) enthalten gültige Daten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="e9ebe-128">0x40</span><span class="sxs-lookup"><span data-stu-id="e9ebe-128">0x40</span></span>    |
| <span data-ttu-id="e9ebe-129">ddpf \_ YUV</span><span class="sxs-lookup"><span data-stu-id="e9ebe-129">DDPF\_YUV</span></span>         | <span data-ttu-id="e9ebe-130">Wird in einigen älteren DDS-Dateien für unkomprimierte YUV-Daten verwendet (dwrgbbitcount enthält die YUV-Bitanzahl; dwrbitmask enthält die Y-Maske, dwgbitmask enthält die U-Maske, dwbbitmask enthält die V-Maske)</span><span class="sxs-lookup"><span data-stu-id="e9ebe-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="e9ebe-131">0x200</span><span class="sxs-lookup"><span data-stu-id="e9ebe-131">0x200</span></span>   |
| <span data-ttu-id="e9ebe-132">ddpf- \_ Leuchtkraft</span><span class="sxs-lookup"><span data-stu-id="e9ebe-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="e9ebe-133">Wird in einigen älteren DDS-Dateien für unkomprimierte Daten mit einer einzelnen Kanal Farbe verwendet (dwrgbbitcount enthält die Bitzahl des leuchtenden Kanals; dwrbitmask enthält die Kanalmaske).</span><span class="sxs-lookup"><span data-stu-id="e9ebe-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="e9ebe-134">Kann mit ddpf- \_ alphapixeln für eine DDS-Datei mit zwei Kanälen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="e9ebe-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="e9ebe-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="e9ebe-136">**dwfourcc**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-137">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-138">Vier Zeichen Codes zum Angeben von komprimierten oder benutzerdefinierten Formaten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="e9ebe-139">Folgende Werte sind möglich: *DXT1*, *DXT2*, *DXT3*, *DXT4* oder *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="e9ebe-140">Ein FourCC von DX10 gibt die vorangestellt den erweiterten Header des [**DDS- \_ Headers \_ DXT10**](dds-header-dxt10.md) an, und der dxgiformat-Member dieser Struktur gibt das echte Format an.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="e9ebe-141">Bei Verwendung eines aus vier Zeichen bestehende Codes müssen dwFlags den *ddpf \_ FourCC* einschließen.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-142">**dwrgbbitcount**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-143">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-144">Anzahl von Bits in einem RGB-Format (möglicherweise einschließlich Alpha).</span><span class="sxs-lookup"><span data-stu-id="e9ebe-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="e9ebe-145">Gültig, wenn **dwFlags** *ddpf \_ RGB*, *ddpf \_ Leucht* Kraft oder *ddpf \_ YUV* umfasst.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-146">**dwrbitmaske**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-147">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-148">Eine rote (oder lumiannce-oder Y-Maske) zum Lesen von Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="e9ebe-149">Bei Angabe des A8R8G8B8-Formats würde die rote Maske beispielsweise 0x00ff0000 lauten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-150">**dwgbitmaske**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-151">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-152">Grüne (oder U) Maske zum Lesen von Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="e9ebe-153">Wenn beispielsweise das Format A8R8G8B8 angegeben ist, wäre die grüne Maske 0x0000ff00.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-154">**dwbbitmask**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-155">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-156">Blaue (oder V-) Maske zum Lesen von Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="e9ebe-157">Bei Angabe des A8R8G8B8-Formats würde die blaue Maske beispielsweise 0x000000ff lauten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="e9ebe-158">**dwabitmask**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="e9ebe-159">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9ebe-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e9ebe-160">Alpha Maske zum Lesen von Alpha-Daten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="e9ebe-161">dwFlags muss *ddpf \_ alphapixels* oder *ddpf \_ Alpha* enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="e9ebe-162">Bei Angabe des A8R8G8B8-Formats würde die Alpha Maske beispielsweise 0xFF000000 lauten.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ebe-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9ebe-163">Remarks</span></span>

<span data-ttu-id="e9ebe-164">Verwenden Sie zum Speichern von DXGI-Formaten, wie z. b. Gleit Komma Daten, die **dwFlags** von ddpf \_ FourCC, und legen Sie **dwfourcc** auf 'd ', ' X ', ' 1 ', ' 0 ' fest.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="e9ebe-165">Verwenden Sie den [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md) -Erweiterungs Header, um das DXGI-Format im **dxgiformat** -Member zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="e9ebe-166">Beachten Sie, dass es nicht standardmäßige Varianten von DDS-Dateien gibt, bei denen **dwFlags** den ddpf \_ FourCC hat und der **dwfourcc** -Wert direkt auf einen D3DFORMAT-oder DXGI- \_ formatenumerationswert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="e9ebe-167">Es ist nicht möglich, die D3DFORMAT-oder DXGI- \_ Format Werte mithilfe dieses nicht standardmäßigen Schemas zu unterscheiden, daher wird stattdessen der DX10-Erweiterungs Header empfohlen.</span><span class="sxs-lookup"><span data-stu-id="e9ebe-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ebe-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9ebe-168">Requirements</span></span>



| <span data-ttu-id="e9ebe-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9ebe-169">Requirement</span></span> | <span data-ttu-id="e9ebe-170">Wert</span><span class="sxs-lookup"><span data-stu-id="e9ebe-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e9ebe-171">Header</span><span class="sxs-lookup"><span data-stu-id="e9ebe-171">Header</span></span><br/> | <dl> <span data-ttu-id="e9ebe-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ebe-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ebe-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ebe-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ebe-174">Verweis für DDS</span><span class="sxs-lookup"><span data-stu-id="e9ebe-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

