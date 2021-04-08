---
description: Definiert die verschiedenen Typen von Oberflächen Formaten.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762108"
---
# <a name="d3dformat"></a><span data-ttu-id="60b0d-103">D3DFORMAT</span><span class="sxs-lookup"><span data-stu-id="60b0d-103">D3DFORMAT</span></span>

<span data-ttu-id="60b0d-104">Definiert die verschiedenen Typen von Oberflächen Formaten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-104">Defines the various types of surface formats.</span></span>

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a><span data-ttu-id="60b0d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60b0d-105">Remarks</span></span>

<span data-ttu-id="60b0d-106">Es gibt verschiedene Arten von Formaten:</span><span class="sxs-lookup"><span data-stu-id="60b0d-106">There are several types of formats:</span></span>

-   [<span data-ttu-id="60b0d-107">BackBuffer-oder Anzeige Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-107">BackBuffer or Display Formats</span></span>](#backbuffer-or-display-formats)
-   [<span data-ttu-id="60b0d-108">Puffer Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-108">Buffer Formats</span></span>](#buffer-formats)
-   [<span data-ttu-id="60b0d-109">Komprimierte DXTn-Textur Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-109">DXTn Compressed Texture Formats</span></span>](#dxtn-compressed-texture-formats)
-   [<span data-ttu-id="60b0d-110">Gleit Komma Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-110">Floating-Point Formats</span></span>](#floating-point-formats)
-   [<span data-ttu-id="60b0d-111">FourCC-Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-111">FOURCC Formats</span></span>](#fourcc-formats)
-   [<span data-ttu-id="60b0d-112">IEEE-Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-112">IEEE Formats</span></span>](#ieee-formats)
-   [<span data-ttu-id="60b0d-113">Gemischte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-113">Mixed Formats</span></span>](#mixed-formats)
-   [<span data-ttu-id="60b0d-114">Signierte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-114">Signed Formats</span></span>](#signed-formats)
-   [<span data-ttu-id="60b0d-115">Nicht signierte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-115">Unsigned Formats</span></span>](#unsigned-formats)
-   [<span data-ttu-id="60b0d-116">Andere</span><span class="sxs-lookup"><span data-stu-id="60b0d-116">Other</span></span>](#other)

<span data-ttu-id="60b0d-117">Alle Formate werden von links nach rechts, das wichtigste Bit bis zum niedrigsten Bit aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-117">All formats are listed from left to right, most-significant bit to least-significant bit.</span></span> <span data-ttu-id="60b0d-118">**D3DFORMAT \_ ARGB** wird z. B. von dem signifikantesten bidirektional a (Alpha) bis zum am wenigsten signifikanten bidirektional B (Blue) geordnet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-118">For example, **D3DFORMAT\_ARGB** is ordered from the most-significant bit channel A (alpha), to the least-significant bit channel B (blue).</span></span> <span data-ttu-id="60b0d-119">Beim Durchlaufen von Surface-Daten werden die Daten im Arbeitsspeicher von dem minimal signifikanten Bit bis zum signifikantesten Bit gespeichert. Dies bedeutet, dass die Channelreihenfolge im Speicher von der niedrigsten (blauen) bis zum höchst wertigen Bit (Alpha) ist.</span><span class="sxs-lookup"><span data-stu-id="60b0d-119">When traversing surface data, the data is stored in memory from least-significant bit to most-significant bit, which means that the channel order in memory is from least-significant bit (blue) to most-significant bit (alpha).</span></span>

<span data-ttu-id="60b0d-120">Der Standardwert für Formate mit nicht definierten Kanälen (G16R16, A8 usw.) ist 1.</span><span class="sxs-lookup"><span data-stu-id="60b0d-120">The default value for formats that contain undefined channels (G16R16, A8, and so on) is 1.</span></span> <span data-ttu-id="60b0d-121">Die einzige Ausnahme ist das A8-Format, das für die drei Farbkanäle mit dem Wert "000" initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="60b0d-121">The only exception is the A8 format, which is initialized to 000 for the three color channels.</span></span>

<span data-ttu-id="60b0d-122">Die Reihenfolge der Bits basiert zuerst auf dem signifikantesten Byte, daher \_ gibt D3DFMT A8L8 an, dass das hohe Byte dieses 2-Byte-Formats Alpha ist.</span><span class="sxs-lookup"><span data-stu-id="60b0d-122">The order of the bits is from the most significant byte first, so D3DFMT\_A8L8 indicates that the high byte of this 2-byte format is alpha.</span></span> <span data-ttu-id="60b0d-123">**D3DFMT \_ D16** gibt einen 16-Bit-ganzzahligen Wert und eine Anwendungs Sperr Bare Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="60b0d-123">**D3DFMT\_D16** indicates a 16-bit integer value and an application-lockable surface.</span></span>

<span data-ttu-id="60b0d-124">Pixel Formate wurden ausgewählt, um den Ausdruck von Hardwarehersteller definierten Erweiterungs Formaten zu aktivieren und die bewährte FourCC-Methode einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-124">Pixel formats have been chosen to enable the expression of hardware-vendor-defined extension formats, as well as to include the well-established FOURCC method.</span></span> <span data-ttu-id="60b0d-125">Der Satz von Formaten, der von der Direct3D-Laufzeit verstanden wird, wird von D3DFORMAT definiert.</span><span class="sxs-lookup"><span data-stu-id="60b0d-125">The set of formats understood by the Direct3D runtime is defined by D3DFORMAT.</span></span>

<span data-ttu-id="60b0d-126">Beachten Sie, dass die Formate von unabhängigen Hardwareanbietern (IHVs) bereitgestellt werden und dass viele FOURCC-Codes nicht aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="60b0d-126">Note that formats are supplied by independent hardware vendors (IHVs) and many FOURCC codes are not listed.</span></span> <span data-ttu-id="60b0d-127">Die Formate in dieser Enumeration sind insofern eindeutig, als Sie von der Laufzeit sanktioniert werden, was bedeutet, dass der verweisrasterizer alle diese Typen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-127">The formats in this enumeration are unique in that they are sanctioned by the runtime, meaning that the reference rasterizer will operate on all these types.</span></span> <span data-ttu-id="60b0d-128">Von IHV bereitgestellte Formate werden von den einzelnen IHVs auf Karten Basis unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60b0d-128">IHV-supplied formats will be supported by the individual IHVs on a card-by-card basis.</span></span>

### <a name="backbuffer-or-display-formats"></a><span data-ttu-id="60b0d-129">BackBuffer-oder Anzeige Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-129">BackBuffer or Display Formats</span></span>

<span data-ttu-id="60b0d-130">Diese Formate sind die einzigen gültigen Formate für einen Hintergrund Puffer oder eine Anzeige.</span><span class="sxs-lookup"><span data-stu-id="60b0d-130">These formats are the only valid formats for a back buffer or a display.</span></span>



| <span data-ttu-id="60b0d-131">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-131">Format</span></span>      | <span data-ttu-id="60b0d-132">Hintergrund Puffer</span><span class="sxs-lookup"><span data-stu-id="60b0d-132">Back buffer</span></span> | <span data-ttu-id="60b0d-133">Anzeige</span><span class="sxs-lookup"><span data-stu-id="60b0d-133">Display</span></span>                   |
|-------------|-------------|---------------------------|
| <span data-ttu-id="60b0d-134">A2R10G10B10</span><span class="sxs-lookup"><span data-stu-id="60b0d-134">A2R10G10B10</span></span> | <span data-ttu-id="60b0d-135">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-135">x</span></span>           | <span data-ttu-id="60b0d-136">x (nur Vollbildmodus)</span><span class="sxs-lookup"><span data-stu-id="60b0d-136">x (full-screen mode only)</span></span> |
| <span data-ttu-id="60b0d-137">A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="60b0d-137">A8R8G8B8</span></span>    | <span data-ttu-id="60b0d-138">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-138">x</span></span>           |                           |
| <span data-ttu-id="60b0d-139">X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="60b0d-139">X8R8G8B8</span></span>    | <span data-ttu-id="60b0d-140">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-140">x</span></span>           | <span data-ttu-id="60b0d-141">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-141">x</span></span>                         |
| <span data-ttu-id="60b0d-142">A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="60b0d-142">A1R5G5B5</span></span>    | <span data-ttu-id="60b0d-143">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-143">x</span></span>           |                           |
| <span data-ttu-id="60b0d-144">X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="60b0d-144">X1R5G5B5</span></span>    | <span data-ttu-id="60b0d-145">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-145">x</span></span>           | <span data-ttu-id="60b0d-146">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-146">x</span></span>                         |
| <span data-ttu-id="60b0d-147">R5G6B5</span><span class="sxs-lookup"><span data-stu-id="60b0d-147">R5G6B5</span></span>      | <span data-ttu-id="60b0d-148">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-148">x</span></span>           | <span data-ttu-id="60b0d-149">x</span><span class="sxs-lookup"><span data-stu-id="60b0d-149">x</span></span>                         |



 

### <a name="buffer-formats"></a><span data-ttu-id="60b0d-150">Puffer Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-150">Buffer Formats</span></span>

<span data-ttu-id="60b0d-151">Tiefe, Schablone, Scheitelpunkt und Index Puffer verfügen jeweils über eindeutige Formate.</span><span class="sxs-lookup"><span data-stu-id="60b0d-151">Depth, stencil, vertex, and index buffers each have unique formats.</span></span>



| <span data-ttu-id="60b0d-152">Pufferflags</span><span class="sxs-lookup"><span data-stu-id="60b0d-152">Buffer flags</span></span>               | <span data-ttu-id="60b0d-153">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-153">Value</span></span> | <span data-ttu-id="60b0d-154">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-154">Format</span></span>                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-155">**D3DFMT \_ D16 \_ Lockable**</span><span class="sxs-lookup"><span data-stu-id="60b0d-155">**D3DFMT\_D16\_LOCKABLE**</span></span>  | <span data-ttu-id="60b0d-156">70</span><span class="sxs-lookup"><span data-stu-id="60b0d-156">70</span></span>    | <span data-ttu-id="60b0d-157">16-Bit-z-Puffer-Bittiefe.</span><span class="sxs-lookup"><span data-stu-id="60b0d-157">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="60b0d-158">**D3DFMT \_ d32**</span><span class="sxs-lookup"><span data-stu-id="60b0d-158">**D3DFMT\_D32**</span></span>            | <span data-ttu-id="60b0d-159">71</span><span class="sxs-lookup"><span data-stu-id="60b0d-159">71</span></span>    | <span data-ttu-id="60b0d-160">32-Bit-z-Puffer-Bittiefe.</span><span class="sxs-lookup"><span data-stu-id="60b0d-160">32-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="60b0d-161">**D3DFMT \_ D15S1**</span><span class="sxs-lookup"><span data-stu-id="60b0d-161">**D3DFMT\_D15S1**</span></span>          | <span data-ttu-id="60b0d-162">73</span><span class="sxs-lookup"><span data-stu-id="60b0d-162">73</span></span>    | <span data-ttu-id="60b0d-163">16-Bit-z-Puffer-bidirektiontiefe, bei der 15 Bits für den tiefen Kanal reserviert sind und ein Bit für den Schablonen Kanal reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="60b0d-163">16-bit z-buffer bit depth where 15 bits are reserved for the depth channel and 1 bit is reserved for the stencil channel.</span></span>                     |
| <span data-ttu-id="60b0d-164">**D3DFMT \_ D24S8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-164">**D3DFMT\_D24S8**</span></span>          | <span data-ttu-id="60b0d-165">75</span><span class="sxs-lookup"><span data-stu-id="60b0d-165">75</span></span>    | <span data-ttu-id="60b0d-166">32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal und 8 Bits für den Schablonen Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-166">32-bit z-buffer bit depth using 24 bits for the depth channel and 8 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="60b0d-167">**D3DFMT \_ D24X8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-167">**D3DFMT\_D24X8**</span></span>          | <span data-ttu-id="60b0d-168">77</span><span class="sxs-lookup"><span data-stu-id="60b0d-168">77</span></span>    | <span data-ttu-id="60b0d-169">32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-169">32-bit z-buffer bit depth using 24 bits for the depth channel.</span></span>                                                                                |
| <span data-ttu-id="60b0d-170">**D3DFMT \_ D24X4S4**</span><span class="sxs-lookup"><span data-stu-id="60b0d-170">**D3DFMT\_D24X4S4**</span></span>        | <span data-ttu-id="60b0d-171">79</span><span class="sxs-lookup"><span data-stu-id="60b0d-171">79</span></span>    | <span data-ttu-id="60b0d-172">32-Bit-z-Puffer Bit Tiefe mit 24 Bits für den tiefen Kanal und 4 Bits für den Schablonen Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-172">32-bit z-buffer bit depth using 24 bits for the depth channel and 4 bits for the stencil channel.</span></span>                                             |
| <span data-ttu-id="60b0d-173">**D3DFMT \_ D32F \_ Lockable**</span><span class="sxs-lookup"><span data-stu-id="60b0d-173">**D3DFMT\_D32F\_LOCKABLE**</span></span> | <span data-ttu-id="60b0d-174">82</span><span class="sxs-lookup"><span data-stu-id="60b0d-174">82</span></span>    | <span data-ttu-id="60b0d-175">Ein Sperr bares Format, bei dem der tiefen Wert als Standard-IEEE-Gleit Komma Zahl dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="60b0d-175">A lockable format where the depth value is represented as a standard IEEE floating-point number.</span></span>                                              |
| <span data-ttu-id="60b0d-176">**D3DFMT \_ D24FS8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-176">**D3DFMT\_D24FS8**</span></span>         | <span data-ttu-id="60b0d-177">83</span><span class="sxs-lookup"><span data-stu-id="60b0d-177">83</span></span>    | <span data-ttu-id="60b0d-178">Ein nicht sperrbares Format, das 24 Bits Tiefe (in einem 24-Bit-Gleit Komma Format-20E4) und 8 Bits der Schablone enthält.</span><span class="sxs-lookup"><span data-stu-id="60b0d-178">A non-lockable format that contains 24 bits of depth (in a 24-bit floating point format - 20e4) and 8 bits of stencil.</span></span>                        |
| <span data-ttu-id="60b0d-179">**D3DFMT \_ d32 \_ Lockable**</span><span class="sxs-lookup"><span data-stu-id="60b0d-179">**D3DFMT\_D32\_LOCKABLE**</span></span>  | <span data-ttu-id="60b0d-180">84</span><span class="sxs-lookup"><span data-stu-id="60b0d-180">84</span></span>    | <span data-ttu-id="60b0d-181">Ein Sperr Bare 32-Bit-Tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="60b0d-181">A lockable 32-bit depth buffer.</span></span> <span data-ttu-id="60b0d-182">**Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60b0d-182">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>  |
| <span data-ttu-id="60b0d-183">**D3DFMT \_ S8 \_ Sperr fähig**</span><span class="sxs-lookup"><span data-stu-id="60b0d-183">**D3DFMT\_S8\_LOCKABLE**</span></span>   | <span data-ttu-id="60b0d-184">85</span><span class="sxs-lookup"><span data-stu-id="60b0d-184">85</span></span>    | <span data-ttu-id="60b0d-185">Ein Sperr bares 8-Bit-Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="60b0d-185">A lockable 8-bit stencil buffer.</span></span> <span data-ttu-id="60b0d-186">**Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60b0d-186">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |
| <span data-ttu-id="60b0d-187">**D3DFMT \_ D16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-187">**D3DFMT\_D16**</span></span>            | <span data-ttu-id="60b0d-188">80</span><span class="sxs-lookup"><span data-stu-id="60b0d-188">80</span></span>    | <span data-ttu-id="60b0d-189">16-Bit-z-Puffer-Bittiefe.</span><span class="sxs-lookup"><span data-stu-id="60b0d-189">16-bit z-buffer bit depth.</span></span>                                                                                                                    |
| <span data-ttu-id="60b0d-190">**D3DFMT \_ vertexdata**</span><span class="sxs-lookup"><span data-stu-id="60b0d-190">**D3DFMT\_VERTEXDATA**</span></span>     | <span data-ttu-id="60b0d-191">100</span><span class="sxs-lookup"><span data-stu-id="60b0d-191">100</span></span>   | <span data-ttu-id="60b0d-192">Beschreibt eine Vertex-Puffer Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="60b0d-192">Describes a vertex buffer surface.</span></span>                                                                                                            |
| <span data-ttu-id="60b0d-193">**D3DFMT \_ INDEX16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-193">**D3DFMT\_INDEX16**</span></span>        | <span data-ttu-id="60b0d-194">101</span><span class="sxs-lookup"><span data-stu-id="60b0d-194">101</span></span>   | <span data-ttu-id="60b0d-195">16-Bit-Index-Puffer Bit Tiefe.</span><span class="sxs-lookup"><span data-stu-id="60b0d-195">16-bit index buffer bit depth.</span></span>                                                                                                                |
| <span data-ttu-id="60b0d-196">**D3DFMT \_ INDEX32**</span><span class="sxs-lookup"><span data-stu-id="60b0d-196">**D3DFMT\_INDEX32**</span></span>        | <span data-ttu-id="60b0d-197">102</span><span class="sxs-lookup"><span data-stu-id="60b0d-197">102</span></span>   | <span data-ttu-id="60b0d-198">32-Bit-Bittiefe des Index Puffers.</span><span class="sxs-lookup"><span data-stu-id="60b0d-198">32-bit index buffer bit depth.</span></span>                                                                                                                |



 

<span data-ttu-id="60b0d-199">Alle tiefen Schablonen Formate mit Ausnahme von D3DFMT \_ D16 \_ Lockable zeigen keine bestimmte bitreihen Folge pro Pixel an, und der Treiber kann mehr als die festgestellte Anzahl von Bits-pro-Tiefe-Kanälen (aber nicht Schablone-Kanal) beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-199">All depth-stencil formats except D3DFMT\_D16\_LOCKABLE indicate no particular bit ordering per pixel, and the driver is allowed to consume more than the indicated number of bits-per-depth channel (but not stencil channel).</span></span>

### <a name="dxtn-compressed-texture-formats"></a><span data-ttu-id="60b0d-200">Komprimierte DXTn-Textur Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-200">DXTn Compressed Texture Formats</span></span>

<span data-ttu-id="60b0d-201">Diese Flags werden für komprimierte Texturen verwendet:</span><span class="sxs-lookup"><span data-stu-id="60b0d-201">These flags are used for compressed textures:</span></span>



| <span data-ttu-id="60b0d-202">Komprimierte DXTn-Textur-Flags</span><span class="sxs-lookup"><span data-stu-id="60b0d-202">DXTn Compressed Texture flags</span></span> | <span data-ttu-id="60b0d-203">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-203">Value</span></span>                          | <span data-ttu-id="60b0d-204">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-204">Format</span></span>                          |
|-------------------------------|--------------------------------|---------------------------------|
| <span data-ttu-id="60b0d-205">**D3DFMT \_ DXT1**</span><span class="sxs-lookup"><span data-stu-id="60b0d-205">**D3DFMT\_DXT1**</span></span>              | <span data-ttu-id="60b0d-206">Makefourcc ("d", "X", "'t", "1")</span><span class="sxs-lookup"><span data-stu-id="60b0d-206">MAKEFOURCC('D', 'X', 'T', '1')</span></span> | <span data-ttu-id="60b0d-207">DXT1 Komprimierungs Textur Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-207">DXT1 compression texture format</span></span> |
| <span data-ttu-id="60b0d-208">**D3DFMT \_ DXT2**</span><span class="sxs-lookup"><span data-stu-id="60b0d-208">**D3DFMT\_DXT2**</span></span>              | <span data-ttu-id="60b0d-209">Makefourcc ("d", "X", "'t", "2")</span><span class="sxs-lookup"><span data-stu-id="60b0d-209">MAKEFOURCC('D', 'X', 'T', '2')</span></span> | <span data-ttu-id="60b0d-210">DXT2 Komprimierungs Textur Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-210">DXT2 compression texture format</span></span> |
| <span data-ttu-id="60b0d-211">**D3DFMT \_ DXT3**</span><span class="sxs-lookup"><span data-stu-id="60b0d-211">**D3DFMT\_DXT3**</span></span>              | <span data-ttu-id="60b0d-212">Makefourcc ("d", "X", "'t", "3")</span><span class="sxs-lookup"><span data-stu-id="60b0d-212">MAKEFOURCC('D', 'X', 'T', '3')</span></span> | <span data-ttu-id="60b0d-213">DXT3 Komprimierungs Textur Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-213">DXT3 compression texture format</span></span> |
| <span data-ttu-id="60b0d-214">**D3DFMT \_ DXT4**</span><span class="sxs-lookup"><span data-stu-id="60b0d-214">**D3DFMT\_DXT4**</span></span>              | <span data-ttu-id="60b0d-215">Makefourcc ("d", "X", "'t", "4")</span><span class="sxs-lookup"><span data-stu-id="60b0d-215">MAKEFOURCC('D', 'X', 'T', '4')</span></span> | <span data-ttu-id="60b0d-216">DXT4 Komprimierungs Textur Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-216">DXT4 compression texture format</span></span> |
| <span data-ttu-id="60b0d-217">**D3DFMT \_ DXT5**</span><span class="sxs-lookup"><span data-stu-id="60b0d-217">**D3DFMT\_DXT5**</span></span>              | <span data-ttu-id="60b0d-218">Makefourcc ("d", "X", "t", "5")</span><span class="sxs-lookup"><span data-stu-id="60b0d-218">MAKEFOURCC('D', 'X', 'T', '5')</span></span> | <span data-ttu-id="60b0d-219">DXT5 Komprimierungs Textur Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-219">DXT5 compression texture format</span></span> |



 

<span data-ttu-id="60b0d-220">Die Laufzeit ermöglicht es einer Anwendung nicht, eine Oberfläche mit einem DXTn-Format zu erstellen, es sei denn, die Oberflächen Dimensionen sind Vielfachen von 4.</span><span class="sxs-lookup"><span data-stu-id="60b0d-220">The runtime will not allow an application to create a surface using a DXTn format unless the surface dimensions are multiples of 4.</span></span> <span data-ttu-id="60b0d-221">Dies gilt für Offscreen-Plain-Flächen, Renderziele, 2D-Texturen, Cube-Texturen und volumetexturen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-221">This applies to offscreen-plain surfaces, render targets, 2D textures, cube textures, and volume textures.</span></span>

### <a name="floating-point-formats"></a><span data-ttu-id="60b0d-222">Floating-Point Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-222">Floating-Point Formats</span></span>

<span data-ttu-id="60b0d-223">Diese Flags werden für Gleit Komma Oberflächen Formate verwendet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-223">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="60b0d-224">Diese 16-Bit-pro-Kanal-Formate werden auch als s10e5-Formate bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-224">These 16-bits-per-channel formats are also known as s10e5 formats.</span></span>



| <span data-ttu-id="60b0d-225">Gleit Komma-Flags</span><span class="sxs-lookup"><span data-stu-id="60b0d-225">Floating-point flags</span></span>      | <span data-ttu-id="60b0d-226">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-226">Value</span></span> | <span data-ttu-id="60b0d-227">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-227">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-228">**D3DFMT \_ R16F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-228">**D3DFMT\_R16F**</span></span>          | <span data-ttu-id="60b0d-229">111</span><span class="sxs-lookup"><span data-stu-id="60b0d-229">111</span></span>   | <span data-ttu-id="60b0d-230">16-Bit-Float-Format mit 16 Bits für den roten Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-230">16-bit float format using 16 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="60b0d-231">**D3DFMT \_ G16R16F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-231">**D3DFMT\_G16R16F**</span></span>       | <span data-ttu-id="60b0d-232">112</span><span class="sxs-lookup"><span data-stu-id="60b0d-232">112</span></span>   | <span data-ttu-id="60b0d-233">32-Bit-Float-Format mit 16 Bits für den roten Kanal und 16 Bits für den grünen Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-233">32-bit float format using 16 bits for the red channel and 16 bits for the green channel.</span></span> |
| <span data-ttu-id="60b0d-234">**D3DFMT \_ A16B16G16R16F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-234">**D3DFMT\_A16B16G16R16F**</span></span> | <span data-ttu-id="60b0d-235">113</span><span class="sxs-lookup"><span data-stu-id="60b0d-235">113</span></span>   | <span data-ttu-id="60b0d-236">64-Bit-Float-Format mit 16 Bits für jeden Kanal (Alpha, blau, grün, rot).</span><span class="sxs-lookup"><span data-stu-id="60b0d-236">64-bit float format using 16 bits for the each channel (alpha, blue, green, red).</span></span>        |



 

### <a name="fourcc-formats"></a><span data-ttu-id="60b0d-237">FourCC-Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-237">FOURCC Formats</span></span>

<span data-ttu-id="60b0d-238">Daten in einem FourCC-Format sind komprimierte Daten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-238">Data in a FOURCC format is compressed data.</span></span>

### <a name="makefourcc"></a><span data-ttu-id="60b0d-239">Makefourcc</span><span class="sxs-lookup"><span data-stu-id="60b0d-239">MAKEFOURCC</span></span>

<span data-ttu-id="60b0d-240">Ein Makro zum Erzeugen von vier Zeichen Codes folgt:</span><span class="sxs-lookup"><span data-stu-id="60b0d-240">A macro for generating four-character codes follows:</span></span>

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

<span data-ttu-id="60b0d-241">Dies sind die definierten FourCC-Formate:</span><span class="sxs-lookup"><span data-stu-id="60b0d-241">Here are the defined FOURCC formats:</span></span>



| <span data-ttu-id="60b0d-242">FourCC-Flags</span><span class="sxs-lookup"><span data-stu-id="60b0d-242">FOURCC flags</span></span>              | <span data-ttu-id="60b0d-243">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-243">Value</span></span>                          | <span data-ttu-id="60b0d-244">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-244">Format</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-245">**D3DFMT \_ MULTI2 \_ ARGB8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-245">**D3DFMT\_MULTI2\_ARGB8**</span></span> | <span data-ttu-id="60b0d-246">Makefourcc ('m ', ' E ', 't ', ' 1 ')</span><span class="sxs-lookup"><span data-stu-id="60b0d-246">MAKEFOURCC('M','E','T','1')</span></span>    | <span data-ttu-id="60b0d-247">Multielement-Textur (nicht komprimiert)</span><span class="sxs-lookup"><span data-stu-id="60b0d-247">MultiElement texture (not compressed)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="60b0d-248">**D3DFMT \_ G8R8 \_ G8B8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-248">**D3DFMT\_G8R8\_G8B8**</span></span>    | <span data-ttu-id="60b0d-249">makefourcc ("g", "R", "g", "B")</span><span class="sxs-lookup"><span data-stu-id="60b0d-249">MAKEFOURCC('G', 'R', 'G', 'B')</span></span> | <span data-ttu-id="60b0d-250">Ein 16-Bit-gepacktes RGB-Format analog zu im YUY2 (Y0U0, Y1V0, Y2U2 usw.).</span><span class="sxs-lookup"><span data-stu-id="60b0d-250">A 16-bit packed RGB format analogous to YUY2 (Y0U0, Y1V0, Y2U2, and so on).</span></span> <span data-ttu-id="60b0d-251">Es ist ein Pixel-paar erforderlich, um den Farbwert ordnungsgemäß darzustellen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-251">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="60b0d-252">Das erste Pixel im Paar enthält 8 Bits von Grün (in den hohen 8 Bits) und 8 Bits rot (in den unteren 8 Bits).</span><span class="sxs-lookup"><span data-stu-id="60b0d-252">The first pixel in the pair contains 8 bits of green (in the high 8 bits) and 8 bits of red (in the low 8 bits).</span></span> <span data-ttu-id="60b0d-253">Das zweite Pixel enthält 8 Bits von Grün (in den großen 8 Bits) und 8 Bits blau (in den unteren 8 Bits).</span><span class="sxs-lookup"><span data-stu-id="60b0d-253">The second pixel contains 8 bits of green (in the high 8 bits) and 8 bits of blue (in the low 8 bits).</span></span> <span data-ttu-id="60b0d-254">Gemeinsam haben die beiden Pixel die roten und blauen Komponenten gemeinsam, während jede über eine eindeutige grüne Komponente verfügt (G0R0, G1B0, G2R2 usw.).</span><span class="sxs-lookup"><span data-stu-id="60b0d-254">Together, the two pixels share the red and blue components, while each has a unique green component (G0R0, G1B0, G2R2, and so on).</span></span> <span data-ttu-id="60b0d-255">Der Textur Sampler normalisiert die Farben bei der Suche in einem Pixelshader nicht. Sie verbleiben im Bereich von 0,0 f bis 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="60b0d-255">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="60b0d-256">Dies gilt für alle programmierbaren Pixel-Shader-Modelle.</span><span class="sxs-lookup"><span data-stu-id="60b0d-256">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="60b0d-257">Für den Pixel-Shader der Fixed-Funktion sollte die Hardware in den Bereich 0. f bis 1. f normalisieren und im Wesentlichen als im YUY2-Textur behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-257">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="60b0d-258">Für Hardware, die dieses Format verfügbar macht, muss der PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt sein, der diesen Bereich verarbeiten darf.</span><span class="sxs-lookup"><span data-stu-id="60b0d-258">Hardware that exposes this format must have the PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span> |
| <span data-ttu-id="60b0d-259">**D3DFMT \_ R8G8 \_ B8G8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-259">**D3DFMT\_R8G8\_B8G8**</span></span>    | <span data-ttu-id="60b0d-260">makefourcc ("R", "g", "B", "g")</span><span class="sxs-lookup"><span data-stu-id="60b0d-260">MAKEFOURCC('R', 'G', 'B', 'G')</span></span> | <span data-ttu-id="60b0d-261">Ein 16-Bit-gepacktes RGB-Format analog zu UYVY (U0Y0, V0Y1, U2Y2 usw.).</span><span class="sxs-lookup"><span data-stu-id="60b0d-261">A 16-bit packed RGB format analogous to UYVY (U0Y0, V0Y1, U2Y2, and so on).</span></span> <span data-ttu-id="60b0d-262">Es ist ein Pixel-paar erforderlich, um den Farbwert ordnungsgemäß darzustellen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-262">It requires a pixel pair in order to properly represent the color value.</span></span> <span data-ttu-id="60b0d-263">Das erste Pixel im Paar enthält 8 Bits von Grün (in den unteren 8 Bits) und 8 Bits rot (in den hohen 8 Bits).</span><span class="sxs-lookup"><span data-stu-id="60b0d-263">The first pixel in the pair contains 8 bits of green (in the low 8 bits) and 8 bits of red (in the high 8 bits).</span></span> <span data-ttu-id="60b0d-264">Das zweite Pixel enthält 8 Bits von Grün (in den unteren 8 Bits) und 8 Bits von blau (in den hohen 8 Bits).</span><span class="sxs-lookup"><span data-stu-id="60b0d-264">The second pixel contains 8 bits of green (in the low 8 bits) and 8 bits of blue (in the high 8 bits).</span></span> <span data-ttu-id="60b0d-265">Gemeinsam haben die beiden Pixel die roten und blauen Komponenten gemeinsam, während jede über eine eindeutige grüne Komponente verfügt (R0G0, B0G1, R2G2 usw.).</span><span class="sxs-lookup"><span data-stu-id="60b0d-265">Together, the two pixels share the red and blue components, while each has a unique green component (R0G0, B0G1, R2G2, and so on).</span></span> <span data-ttu-id="60b0d-266">Der Textur Sampler normalisiert die Farben bei der Suche in einem Pixelshader nicht. Sie verbleiben im Bereich von 0,0 f bis 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="60b0d-266">The texture sampler does not normalize the colors when looking up into a pixel shader; they remain in the range of 0.0f to 255.0f.</span></span> <span data-ttu-id="60b0d-267">Dies gilt für alle programmierbaren Pixel-Shader-Modelle.</span><span class="sxs-lookup"><span data-stu-id="60b0d-267">This is true for all programmable pixel shader models.</span></span> <span data-ttu-id="60b0d-268">Für den Pixel-Shader der Fixed-Funktion sollte die Hardware in den Bereich 0. f bis 1. f normalisieren und im Wesentlichen als im YUY2-Textur behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-268">For the fixed function pixel shader, the hardware should normalize to the 0.f to 1.f range and essentially treat it as the YUY2 texture.</span></span> <span data-ttu-id="60b0d-269">Für Hardware, die dieses Format verfügbar macht, muss der PixelShader1xMaxValue-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) auf einen Wert festgelegt werden, der diesen Bereich verarbeiten darf.</span><span class="sxs-lookup"><span data-stu-id="60b0d-269">Hardware that exposes this format must have PixelShader1xMaxValue member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) set to a value capable of handling that range.</span></span>     |
| <span data-ttu-id="60b0d-270">**D3DFMT \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="60b0d-270">**D3DFMT\_UYVY**</span></span>          | <span data-ttu-id="60b0d-271">makefourcc ("U", "y", "V", "y")</span><span class="sxs-lookup"><span data-stu-id="60b0d-271">MAKEFOURCC('U', 'Y', 'V', 'Y')</span></span> | <span data-ttu-id="60b0d-272">UYVY-Format (PC98-Konformität)</span><span class="sxs-lookup"><span data-stu-id="60b0d-272">UYVY format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="60b0d-273">**D3DFMT \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="60b0d-273">**D3DFMT\_YUY2**</span></span>          | <span data-ttu-id="60b0d-274">Makefourcc ("y", "U", "y", "2")</span><span class="sxs-lookup"><span data-stu-id="60b0d-274">MAKEFOURCC('Y', 'U', 'Y', '2')</span></span> | <span data-ttu-id="60b0d-275">Im YUY2-Format (PC98-Konformität)</span><span class="sxs-lookup"><span data-stu-id="60b0d-275">YUY2 format (PC98 compliance)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a><span data-ttu-id="60b0d-276">IEEE-Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-276">IEEE Formats</span></span>

<span data-ttu-id="60b0d-277">Diese Flags werden für Gleit Komma Oberflächen Formate verwendet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-277">These flags are used for floating-point surface formats.</span></span> <span data-ttu-id="60b0d-278">Diese 32-Bits-pro-Channel-Formate werden auch als s23e8-Formate bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-278">These 32-bits-per-channel formats are also known as s23e8 formats.</span></span>



| <span data-ttu-id="60b0d-279">Gleit Komma-Flags</span><span class="sxs-lookup"><span data-stu-id="60b0d-279">Floating-point flags</span></span>      | <span data-ttu-id="60b0d-280">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-280">Value</span></span> | <span data-ttu-id="60b0d-281">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-281">Format</span></span>                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-282">**D3DFMT \_ R32F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-282">**D3DFMT\_R32F**</span></span>          | <span data-ttu-id="60b0d-283">114</span><span class="sxs-lookup"><span data-stu-id="60b0d-283">114</span></span>   | <span data-ttu-id="60b0d-284">32-Bit-Float-Format unter Verwendung von 32 Bits für den roten Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-284">32-bit float format using 32 bits for the red channel.</span></span>                                   |
| <span data-ttu-id="60b0d-285">**D3DFMT \_ G32R32F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-285">**D3DFMT\_G32R32F**</span></span>       | <span data-ttu-id="60b0d-286">115</span><span class="sxs-lookup"><span data-stu-id="60b0d-286">115</span></span>   | <span data-ttu-id="60b0d-287">64-Bit-Float-Format unter Verwendung von 32 Bits für den roten Kanal und 32 Bits für den grünen Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-287">64-bit float format using 32 bits for the red channel and 32 bits for the green channel.</span></span> |
| <span data-ttu-id="60b0d-288">**D3DFMT \_ A32B32G32R32F**</span><span class="sxs-lookup"><span data-stu-id="60b0d-288">**D3DFMT\_A32B32G32R32F**</span></span> | <span data-ttu-id="60b0d-289">116</span><span class="sxs-lookup"><span data-stu-id="60b0d-289">116</span></span>   | <span data-ttu-id="60b0d-290">128-Bit-Float-Format unter Verwendung von 32 Bits für jeden Kanal (Alpha, blau, grün, rot).</span><span class="sxs-lookup"><span data-stu-id="60b0d-290">128-bit float format using 32 bits for the each channel (alpha, blue, green, red).</span></span>       |



 

### <a name="mixed-formats"></a><span data-ttu-id="60b0d-291">Gemischte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-291">Mixed Formats</span></span>

<span data-ttu-id="60b0d-292">Daten in gemischten Formaten können eine Kombination aus nicht signierten Daten und signierten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-292">Data in mixed formats can contain a combination of unsigned data and signed data.</span></span>



| <span data-ttu-id="60b0d-293">Gemischte Formatflags</span><span class="sxs-lookup"><span data-stu-id="60b0d-293">Mixed format flags</span></span>      | <span data-ttu-id="60b0d-294">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-294">Value</span></span> | <span data-ttu-id="60b0d-295">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-295">Format</span></span>                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-296">**D3DFMT \_ L6V5U5**</span><span class="sxs-lookup"><span data-stu-id="60b0d-296">**D3DFMT\_L6V5U5**</span></span>      | <span data-ttu-id="60b0d-297">61</span><span class="sxs-lookup"><span data-stu-id="60b0d-297">61</span></span>    | <span data-ttu-id="60b0d-298">16-Bit-Bump-Map-Format mit Leuchtkraft, das 6 Bits für die Leuchtkraft verwendet, und 5 Bits für v und Sie.</span><span class="sxs-lookup"><span data-stu-id="60b0d-298">16-bit bump-map format with luminance using 6 bits for luminance, and 5 bits each for v and u.</span></span> |
| <span data-ttu-id="60b0d-299">**D3DFMT \_ X8L8V8U8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-299">**D3DFMT\_X8L8V8U8**</span></span>    | <span data-ttu-id="60b0d-300">62</span><span class="sxs-lookup"><span data-stu-id="60b0d-300">62</span></span>    | <span data-ttu-id="60b0d-301">32-Bit-Bump-Map-Format mit der Leuchtkraft, wobei für jeden Kanal 8 Bits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-301">32-bit bump-map format with luminance using 8 bits for each channel.</span></span>                           |
| <span data-ttu-id="60b0d-302">**D3DFMT \_ A2W10V10U10**</span><span class="sxs-lookup"><span data-stu-id="60b0d-302">**D3DFMT\_A2W10V10U10**</span></span> | <span data-ttu-id="60b0d-303">67</span><span class="sxs-lookup"><span data-stu-id="60b0d-303">67</span></span>    | <span data-ttu-id="60b0d-304">32-Bit-Bump-Map-Format, bei dem 2 Bits für Alpha und 10 Bits für w, v und Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-304">32-bit bump-map format using 2 bits for alpha and 10 bits each for w, v, and u.</span></span>                |



 

### <a name="signed-formats"></a><span data-ttu-id="60b0d-305">Signierte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-305">Signed Formats</span></span>

<span data-ttu-id="60b0d-306">Daten in einem signierten Format können sowohl positiv als auch negativ sein.</span><span class="sxs-lookup"><span data-stu-id="60b0d-306">Data in a signed format can be both positive and negative.</span></span> <span data-ttu-id="60b0d-307">Signierte Formate verwenden Kombinationen von (U), (V), (W) und (Q)-Daten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-307">Signed formats use combinations of (U), (V), (W), and (Q) data.</span></span>



| <span data-ttu-id="60b0d-308">Signierte Formatflags</span><span class="sxs-lookup"><span data-stu-id="60b0d-308">Signed format flags</span></span>      | <span data-ttu-id="60b0d-309">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-309">Value</span></span> | <span data-ttu-id="60b0d-310">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-310">Format</span></span>                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-311">**D3DFMT \_ V8U8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-311">**D3DFMT\_V8U8**</span></span>         | <span data-ttu-id="60b0d-312">60</span><span class="sxs-lookup"><span data-stu-id="60b0d-312">60</span></span>    | <span data-ttu-id="60b0d-313">16-Bit-Bump-Map-Format mit jeweils 8 Bits für Sie und v-Daten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-313">16-bit bump-map format using 8 bits each for u and v data.</span></span>                                                |
| <span data-ttu-id="60b0d-314">**D3DFMT \_ Q8W8V8U8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-314">**D3DFMT\_Q8W8V8U8**</span></span>     | <span data-ttu-id="60b0d-315">63</span><span class="sxs-lookup"><span data-stu-id="60b0d-315">63</span></span>    | <span data-ttu-id="60b0d-316">32-Bit-Bump-Map-Format, bei dem für jeden Kanal 8 Bits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-316">32-bit bump-map format using 8 bits for each channel.</span></span>                                                     |
| <span data-ttu-id="60b0d-317">**D3DFMT \_ V16U16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-317">**D3DFMT\_V16U16**</span></span>       | <span data-ttu-id="60b0d-318">64</span><span class="sxs-lookup"><span data-stu-id="60b0d-318">64</span></span>    | <span data-ttu-id="60b0d-319">32-Bit-Bump-Map-Format mit 16 Bits für jeden Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-319">32-bit bump-map format using 16 bits for each channel.</span></span>                                                    |
| <span data-ttu-id="60b0d-320">**D3DFMT \_ Q16W16V16U16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-320">**D3DFMT\_Q16W16V16U16**</span></span> | <span data-ttu-id="60b0d-321">110</span><span class="sxs-lookup"><span data-stu-id="60b0d-321">110</span></span>   | <span data-ttu-id="60b0d-322">64-Bit-Bump-Map-Format mit 16 Bits für jede Komponente.</span><span class="sxs-lookup"><span data-stu-id="60b0d-322">64-bit bump-map format using 16 bits for each component.</span></span>                                                  |
| <span data-ttu-id="60b0d-323">**D3DFMT \_ CxV8U8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-323">**D3DFMT\_CxV8U8**</span></span>       | <span data-ttu-id="60b0d-324">117</span><span class="sxs-lookup"><span data-stu-id="60b0d-324">117</span></span>   | <span data-ttu-id="60b0d-325">normales 16-Bit-Komprimierungs Format.</span><span class="sxs-lookup"><span data-stu-id="60b0d-325">16-bit normal compression format.</span></span> <span data-ttu-id="60b0d-326">Der Textur Sampler berechnet den c-Kanal von: c = sqrt (1-U ²-V ²).</span><span class="sxs-lookup"><span data-stu-id="60b0d-326">The texture sampler computes the C channel from: C = sqrt(1 - U² - V²).</span></span> |



 

### <a name="unsigned-formats"></a><span data-ttu-id="60b0d-327">Nicht signierte Formate</span><span class="sxs-lookup"><span data-stu-id="60b0d-327">Unsigned Formats</span></span>

<span data-ttu-id="60b0d-328">Daten in einem unsignierten Format müssen positiv sein.</span><span class="sxs-lookup"><span data-stu-id="60b0d-328">Data in an unsigned format must be positive.</span></span> <span data-ttu-id="60b0d-329">Unsignierte Formate verwenden Kombinationen von (R) Ed-, (G) Reen, (B) Lue, (A) lpha, (L) uminance und (P) Alette Daten.</span><span class="sxs-lookup"><span data-stu-id="60b0d-329">Unsigned formats use combinations of (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance, and (P)alette data.</span></span> <span data-ttu-id="60b0d-330">Palettendaten werden auch als Farb indizierte Daten bezeichnet, da die Daten zum Indizieren einer Farbpalette verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-330">Palette data is also referred to as color indexed data because the data is used to index a color palette.</span></span>



| <span data-ttu-id="60b0d-331">Nicht signierte Formatflags</span><span class="sxs-lookup"><span data-stu-id="60b0d-331">Unsigned format flags</span></span>             | <span data-ttu-id="60b0d-332">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-332">Value</span></span> | <span data-ttu-id="60b0d-333">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-333">Format</span></span>                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-334">**D3DFMT \_ R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-334">**D3DFMT\_R8G8B8**</span></span>                | <span data-ttu-id="60b0d-335">20</span><span class="sxs-lookup"><span data-stu-id="60b0d-335">20</span></span>    | <span data-ttu-id="60b0d-336">24-Bit-RGB-Pixel-Format mit 8 Bits pro Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-336">24-bit RGB pixel format with 8 bits per channel.</span></span>                                                                                                                          |
| <span data-ttu-id="60b0d-337">**D3DFMT \_ A8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-337">**D3DFMT\_A8R8G8B8**</span></span>              | <span data-ttu-id="60b0d-338">21</span><span class="sxs-lookup"><span data-stu-id="60b0d-338">21</span></span>    | <span data-ttu-id="60b0d-339">32-Bit-ARGB-Pixel Format mit Alpha, bei dem 8 Bits pro Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-339">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="60b0d-340">**D3DFMT \_ X8R8G8B8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-340">**D3DFMT\_X8R8G8B8**</span></span>              | <span data-ttu-id="60b0d-341">22</span><span class="sxs-lookup"><span data-stu-id="60b0d-341">22</span></span>    | <span data-ttu-id="60b0d-342">32-Bit-RGB-Pixel Format, bei dem 8 Bits für jede Farbe reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="60b0d-342">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="60b0d-343">**D3DFMT \_ R5G6B5**</span><span class="sxs-lookup"><span data-stu-id="60b0d-343">**D3DFMT\_R5G6B5**</span></span>                | <span data-ttu-id="60b0d-344">23</span><span class="sxs-lookup"><span data-stu-id="60b0d-344">23</span></span>    | <span data-ttu-id="60b0d-345">16-Bit-RGB-Pixel-Format mit 5 Bits für Rot, 6 Bits für Grün und 5 Bits für blau.</span><span class="sxs-lookup"><span data-stu-id="60b0d-345">16-bit RGB pixel format with 5 bits for red, 6 bits for green, and 5 bits for blue.</span></span>                                                                                       |
| <span data-ttu-id="60b0d-346">**D3DFMT \_ X1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="60b0d-346">**D3DFMT\_X1R5G5B5**</span></span>              | <span data-ttu-id="60b0d-347">24</span><span class="sxs-lookup"><span data-stu-id="60b0d-347">24</span></span>    | <span data-ttu-id="60b0d-348">16-Bit-Pixel Format, bei dem 5 Bits für jede Farbe reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="60b0d-348">16-bit pixel format where 5 bits are reserved for each color.</span></span>                                                                                                             |
| <span data-ttu-id="60b0d-349">**D3DFMT \_ A1R5G5B5**</span><span class="sxs-lookup"><span data-stu-id="60b0d-349">**D3DFMT\_A1R5G5B5**</span></span>              | <span data-ttu-id="60b0d-350">25</span><span class="sxs-lookup"><span data-stu-id="60b0d-350">25</span></span>    | <span data-ttu-id="60b0d-351">16-Bit-Pixel Format, bei dem 5 Bits für jede Farbe reserviert sind und ein Bit für Alpha reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="60b0d-351">16-bit pixel format where 5 bits are reserved for each color and 1 bit is reserved for alpha.</span></span>                                                                             |
| <span data-ttu-id="60b0d-352">**D3DFMT \_ A4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="60b0d-352">**D3DFMT\_A4R4G4B4**</span></span>              | <span data-ttu-id="60b0d-353">26</span><span class="sxs-lookup"><span data-stu-id="60b0d-353">26</span></span>    | <span data-ttu-id="60b0d-354">16-Bit-ARGB-Pixel Format mit 4 Bits für jeden Kanal.</span><span class="sxs-lookup"><span data-stu-id="60b0d-354">16-bit ARGB pixel format with 4 bits for each channel.</span></span>                                                                                                                    |
| <span data-ttu-id="60b0d-355">**D3DFMT \_ R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="60b0d-355">**D3DFMT\_R3G3B2**</span></span>                | <span data-ttu-id="60b0d-356">27</span><span class="sxs-lookup"><span data-stu-id="60b0d-356">27</span></span>    | <span data-ttu-id="60b0d-357">8-Bit-RGB-Textur Format mit 3 Bits für Rot, 3 Bits für Grün und 2 Bits für blau.</span><span class="sxs-lookup"><span data-stu-id="60b0d-357">8-bit RGB texture format using 3 bits for red, 3 bits for green, and 2 bits for blue.</span></span>                                                                                     |
| <span data-ttu-id="60b0d-358">**D3DFMT \_ a8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-358">**D3DFMT\_A8**</span></span>                    | <span data-ttu-id="60b0d-359">28</span><span class="sxs-lookup"><span data-stu-id="60b0d-359">28</span></span>    | <span data-ttu-id="60b0d-360">nur 8-Bit-Alpha.</span><span class="sxs-lookup"><span data-stu-id="60b0d-360">8-bit alpha only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="60b0d-361">**D3DFMT \_ A8R3G3B2**</span><span class="sxs-lookup"><span data-stu-id="60b0d-361">**D3DFMT\_A8R3G3B2**</span></span>              | <span data-ttu-id="60b0d-362">29</span><span class="sxs-lookup"><span data-stu-id="60b0d-362">29</span></span>    | <span data-ttu-id="60b0d-363">ein 16-Bit-ARGB-Textur Format mit 8 Bits für Alpha, 3 Bits für Rot und grün und 2 Bits für blau.</span><span class="sxs-lookup"><span data-stu-id="60b0d-363">16-bit ARGB texture format using 8 bits for alpha, 3 bits each for red and green, and 2 bits for blue.</span></span>                                                                    |
| <span data-ttu-id="60b0d-364">**D3DFMT \_ X4R4G4B4**</span><span class="sxs-lookup"><span data-stu-id="60b0d-364">**D3DFMT\_X4R4G4B4**</span></span>              | <span data-ttu-id="60b0d-365">30</span><span class="sxs-lookup"><span data-stu-id="60b0d-365">30</span></span>    | <span data-ttu-id="60b0d-366">16-Bit-RGB-Pixel-Format mit 4 Bits für jede Farbe.</span><span class="sxs-lookup"><span data-stu-id="60b0d-366">16-bit RGB pixel format using 4 bits for each color.</span></span>                                                                                                                      |
| <span data-ttu-id="60b0d-367">**D3DFMT \_ A2B10G10R10**</span><span class="sxs-lookup"><span data-stu-id="60b0d-367">**D3DFMT\_A2B10G10R10**</span></span>           | <span data-ttu-id="60b0d-368">31</span><span class="sxs-lookup"><span data-stu-id="60b0d-368">31</span></span>    | <span data-ttu-id="60b0d-369">32-Bit-Pixel Format mit 10 Bits für jede Farbe und 2 Bits für Alpha.</span><span class="sxs-lookup"><span data-stu-id="60b0d-369">32-bit pixel format using 10 bits for each color and 2 bits for alpha.</span></span>                                                                                                    |
| <span data-ttu-id="60b0d-370">**D3DFMT \_ A8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-370">**D3DFMT\_A8B8G8R8**</span></span>              | <span data-ttu-id="60b0d-371">32</span><span class="sxs-lookup"><span data-stu-id="60b0d-371">32</span></span>    | <span data-ttu-id="60b0d-372">32-Bit-ARGB-Pixel Format mit Alpha, bei dem 8 Bits pro Kanal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60b0d-372">32-bit ARGB pixel format with alpha, using 8 bits per channel.</span></span>                                                                                                            |
| <span data-ttu-id="60b0d-373">**D3DFMT \_ X8B8G8R8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-373">**D3DFMT\_X8B8G8R8**</span></span>              | <span data-ttu-id="60b0d-374">33</span><span class="sxs-lookup"><span data-stu-id="60b0d-374">33</span></span>    | <span data-ttu-id="60b0d-375">32-Bit-RGB-Pixel Format, bei dem 8 Bits für jede Farbe reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="60b0d-375">32-bit RGB pixel format, where 8 bits are reserved for each color.</span></span>                                                                                                        |
| <span data-ttu-id="60b0d-376">**D3DFMT \_ G16R16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-376">**D3DFMT\_G16R16**</span></span>                | <span data-ttu-id="60b0d-377">34</span><span class="sxs-lookup"><span data-stu-id="60b0d-377">34</span></span>    | <span data-ttu-id="60b0d-378">32-Bit-Pixel Format mit jeweils 16 Bits für Grün und rot.</span><span class="sxs-lookup"><span data-stu-id="60b0d-378">32-bit pixel format using 16 bits each for green and red.</span></span>                                                                                                                 |
| <span data-ttu-id="60b0d-379">**D3DFMT \_ A2R10G10B10**</span><span class="sxs-lookup"><span data-stu-id="60b0d-379">**D3DFMT\_A2R10G10B10**</span></span>           | <span data-ttu-id="60b0d-380">35</span><span class="sxs-lookup"><span data-stu-id="60b0d-380">35</span></span>    | <span data-ttu-id="60b0d-381">32-Bit-Pixel Format mit jeweils 10 Bits für Rot, grün und blau und 2 Bits für Alpha.</span><span class="sxs-lookup"><span data-stu-id="60b0d-381">32-bit pixel format using 10 bits each for red, green, and blue, and 2 bits for alpha.</span></span>                                                                                    |
| <span data-ttu-id="60b0d-382">**D3DFMT \_ A16B16G16R16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-382">**D3DFMT\_A16B16G16R16**</span></span>          | <span data-ttu-id="60b0d-383">36</span><span class="sxs-lookup"><span data-stu-id="60b0d-383">36</span></span>    | <span data-ttu-id="60b0d-384">64-Bit-Pixel Format mit 16 Bits für jede Komponente.</span><span class="sxs-lookup"><span data-stu-id="60b0d-384">64-bit pixel format using 16 bits for each component.</span></span>                                                                                                                     |
| <span data-ttu-id="60b0d-385">**D3DFMT \_ A8P8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-385">**D3DFMT\_A8P8**</span></span>                  | <span data-ttu-id="60b0d-386">40</span><span class="sxs-lookup"><span data-stu-id="60b0d-386">40</span></span>    | <span data-ttu-id="60b0d-387">8-Bit-Farbe mit 8 Bits Alpha indiziert.</span><span class="sxs-lookup"><span data-stu-id="60b0d-387">8-bit color indexed with 8 bits of alpha.</span></span>                                                                                                                                 |
| <span data-ttu-id="60b0d-388">**D3DFMT \_ P8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-388">**D3DFMT\_P8**</span></span>                    | <span data-ttu-id="60b0d-389">41</span><span class="sxs-lookup"><span data-stu-id="60b0d-389">41</span></span>    | <span data-ttu-id="60b0d-390">8-Bit-Farbe indiziert.</span><span class="sxs-lookup"><span data-stu-id="60b0d-390">8-bit color indexed.</span></span>                                                                                                                                                      |
| <span data-ttu-id="60b0d-391">**D3DFMT \_ L8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-391">**D3DFMT\_L8**</span></span>                    | <span data-ttu-id="60b0d-392">50</span><span class="sxs-lookup"><span data-stu-id="60b0d-392">50</span></span>    | <span data-ttu-id="60b0d-393">nur 8-Bit-Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="60b0d-393">8-bit luminance only.</span></span>                                                                                                                                                     |
| <span data-ttu-id="60b0d-394">**D3DFMT \_ L16**</span><span class="sxs-lookup"><span data-stu-id="60b0d-394">**D3DFMT\_L16**</span></span>                   | <span data-ttu-id="60b0d-395">81</span><span class="sxs-lookup"><span data-stu-id="60b0d-395">81</span></span>    | <span data-ttu-id="60b0d-396">nur 16-Bit-Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="60b0d-396">16-bit luminance only.</span></span>                                                                                                                                                    |
| <span data-ttu-id="60b0d-397">**D3DFMT \_ A8L8**</span><span class="sxs-lookup"><span data-stu-id="60b0d-397">**D3DFMT\_A8L8**</span></span>                  | <span data-ttu-id="60b0d-398">51</span><span class="sxs-lookup"><span data-stu-id="60b0d-398">51</span></span>    | <span data-ttu-id="60b0d-399">16 Bit mit jeweils 8 Bits für Alpha und Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="60b0d-399">16-bit using 8 bits each for alpha and luminance.</span></span>                                                                                                                         |
| <span data-ttu-id="60b0d-400">**D3DFMT \_ A4L4**</span><span class="sxs-lookup"><span data-stu-id="60b0d-400">**D3DFMT\_A4L4**</span></span>                  | <span data-ttu-id="60b0d-401">52</span><span class="sxs-lookup"><span data-stu-id="60b0d-401">52</span></span>    | <span data-ttu-id="60b0d-402">8-Bit mit jeweils 4 Bits für Alpha und Leuchtkraft.</span><span class="sxs-lookup"><span data-stu-id="60b0d-402">8-bit using 4 bits each for alpha and luminance.</span></span>                                                                                                                          |
| <span data-ttu-id="60b0d-403">**D3DFMT \_ a1**</span><span class="sxs-lookup"><span data-stu-id="60b0d-403">**D3DFMT\_A1**</span></span>                    | <span data-ttu-id="60b0d-404">118</span><span class="sxs-lookup"><span data-stu-id="60b0d-404">118</span></span>   | <span data-ttu-id="60b0d-405">1-Bit-Monochrome.</span><span class="sxs-lookup"><span data-stu-id="60b0d-405">1-bit monochrome.</span></span> <span data-ttu-id="60b0d-406">**Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60b0d-406">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                            |
| <span data-ttu-id="60b0d-407">**D3DFMT \_ A2B10G10R10 \_ XR- \_ Bias**</span><span class="sxs-lookup"><span data-stu-id="60b0d-407">**D3DFMT\_A2B10G10R10\_XR\_BIAS**</span></span> | <span data-ttu-id="60b0d-408">119</span><span class="sxs-lookup"><span data-stu-id="60b0d-408">119</span></span>   | <span data-ttu-id="60b0d-409">2,8-seitiger fester Punkt.</span><span class="sxs-lookup"><span data-stu-id="60b0d-409">2.8-biased fixed point.</span></span> <span data-ttu-id="60b0d-410">**Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60b0d-410">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/>                                      |
| <span data-ttu-id="60b0d-411">**D3DFMT \_ binaryBuffer**</span><span class="sxs-lookup"><span data-stu-id="60b0d-411">**D3DFMT\_BINARYBUFFER**</span></span>          | <span data-ttu-id="60b0d-412">199</span><span class="sxs-lookup"><span data-stu-id="60b0d-412">199</span></span>   | <span data-ttu-id="60b0d-413">Binärformat, das angibt, dass die Daten keinen inhärenten Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="60b0d-413">Binary format indicating that the data has no inherent type.</span></span> <span data-ttu-id="60b0d-414">**Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:** Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60b0d-414">**Differences between Direct3D 9 and Direct3D 9Ex:** This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

### <a name="other"></a><span data-ttu-id="60b0d-415">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="60b0d-415">Other</span></span>

<span data-ttu-id="60b0d-416">Dieses Flag wird für nicht definierte Formate verwendet.</span><span class="sxs-lookup"><span data-stu-id="60b0d-416">This flag is used for undefined formats.</span></span>



| <span data-ttu-id="60b0d-417">Andere Flags</span><span class="sxs-lookup"><span data-stu-id="60b0d-417">Other flags</span></span>         | <span data-ttu-id="60b0d-418">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-418">Value</span></span> | <span data-ttu-id="60b0d-419">Format</span><span class="sxs-lookup"><span data-stu-id="60b0d-419">Format</span></span>                    |
|---------------------|-------|---------------------------|
| <span data-ttu-id="60b0d-420">**D3DFMT \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="60b0d-420">**D3DFMT\_UNKNOWN**</span></span> | <span data-ttu-id="60b0d-421">0</span><span class="sxs-lookup"><span data-stu-id="60b0d-421">0</span></span>     | <span data-ttu-id="60b0d-422">Das Oberflächen Format ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="60b0d-422">Surface format is unknown</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="60b0d-423">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b0d-423">Requirements</span></span>



| <span data-ttu-id="60b0d-424">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b0d-424">Requirement</span></span> | <span data-ttu-id="60b0d-425">Wert</span><span class="sxs-lookup"><span data-stu-id="60b0d-425">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b0d-426">Header</span><span class="sxs-lookup"><span data-stu-id="60b0d-426">Header</span></span><br/> | <dl> <span data-ttu-id="60b0d-427"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b0d-427"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b0d-428">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b0d-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b0d-429">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="60b0d-429">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




