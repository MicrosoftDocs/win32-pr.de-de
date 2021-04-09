---
description: Definiert Konstanten, die die unterstützten Textur Adressierungs Modi beschreiben.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: D3DTEXTUREADDRESS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050842"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="724a8-103">D3DTEXTUREADDRESS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="724a8-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="724a8-104">Definiert Konstanten, die die unterstützten Textur Adressierungs Modi beschreiben.</span><span class="sxs-lookup"><span data-stu-id="724a8-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="724a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="724a8-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="724a8-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="724a8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="724a8-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Wrap**</span><span class="sxs-lookup"><span data-stu-id="724a8-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-108">Kacheln Sie die Textur bei jeder ganzzahligen Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="724a8-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="724a8-109">Wenn Sie z. b. Werte zwischen 0 und 3 haben, wird die Textur dreimal wiederholt. Es wird keine Spiegelung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="724a8-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="724a8-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS- \_ Spiegelung**</span><span class="sxs-lookup"><span data-stu-id="724a8-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-111">Vergleichbar mit D3DTADDRESS \_ Wrap, mit der Ausnahme, dass die Textur bei jeder ganzzahligen Verknüpfung gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="724a8-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="724a8-112">bei Werten zwischen 0 und 1 wird die Textur z. b. normal behandelt. zwischen 1 und 2 wird die Textur gekippt (gespiegelt). zwischen 2 und 3 ist die Textur wieder normal. Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="724a8-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="724a8-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS- \_ Klammer**</span><span class="sxs-lookup"><span data-stu-id="724a8-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-114">Texturkoordinaten außerhalb des Bereichs \[ 0,0, 1,0 \] werden auf die Textur Farbe bei 0,0 oder 1,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="724a8-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="724a8-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS \_ -Rahmen**</span><span class="sxs-lookup"><span data-stu-id="724a8-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-116">Texturkoordinaten außerhalb des Bereichs \[ 0,0, 1,0 \] werden auf die Rahmenfarbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="724a8-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="724a8-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ mirroronce**</span><span class="sxs-lookup"><span data-stu-id="724a8-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-118">Vergleichbar mit D3DTADDRESS \_ Mirror und D3DTADDRESS \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="724a8-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="724a8-119">Nimmt den absoluten Wert der Textur Koordinate (also die Spiegelung um 0) und bindet dann an den maximalen Wert.</span><span class="sxs-lookup"><span data-stu-id="724a8-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="724a8-120">Die häufigste Verwendung ist für volumetexturen, bei denen die Unterstützung für den vollständigen D3DTADDRESS \_ mirroronce-Textur Adressierungs Modus nicht erforderlich ist, aber die Daten um die eine Achse symmetrisch sind.</span><span class="sxs-lookup"><span data-stu-id="724a8-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="724a8-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="724a8-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="724a8-122">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="724a8-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="724a8-123">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="724a8-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="724a8-124">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="724a8-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="724a8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="724a8-125">Requirements</span></span>



| <span data-ttu-id="724a8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="724a8-126">Requirement</span></span> | <span data-ttu-id="724a8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="724a8-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="724a8-128">Header</span><span class="sxs-lookup"><span data-stu-id="724a8-128">Header</span></span><br/> | <dl> <span data-ttu-id="724a8-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="724a8-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724a8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="724a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724a8-131">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="724a8-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="724a8-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="724a8-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
