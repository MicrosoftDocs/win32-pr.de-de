---
description: Beschreibt die Auflösung des Schatten-z-Puffers, der in der direkt Beleuchtungs Simulation der vorab berechneten Strahlen Übertragung (PRT) auf der GPU verwendet wird.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: D3DXSHGPUSIMOPT-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350717"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="be317-103">D3DXSHGPUSIMOPT-Enumeration</span><span class="sxs-lookup"><span data-stu-id="be317-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="be317-104">Beschreibt die Auflösung des Schatten-z-Puffers, der in der direkt Beleuchtungs Simulation der vorab berechneten Strahlen Übertragung (PRT) auf der GPU verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be317-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="be317-105">Ein z-Puffer mit höherer Qualität kann auch angegeben werden, um das Rauschen der Ergebnisse der direkt Beleuchtungs Simulation zu reduzieren, obwohl die Simulation langsamer ist.</span><span class="sxs-lookup"><span data-stu-id="be317-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="be317-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="be317-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="be317-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="be317-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be317-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="be317-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="be317-109">Simulation mit niedriger Auflösung.</span><span class="sxs-lookup"><span data-stu-id="be317-109">Low resolution simulation.</span></span> <span data-ttu-id="be317-110">In der Simulation wird eine 256 x 256 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.</span><span class="sxs-lookup"><span data-stu-id="be317-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="be317-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="be317-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="be317-112">Simulation mit mittlerer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="be317-112">Medium resolution simulation.</span></span> <span data-ttu-id="be317-113">In der Simulation wird eine 512 x 512 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.</span><span class="sxs-lookup"><span data-stu-id="be317-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="be317-114">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="be317-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="be317-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="be317-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="be317-116">Hochauflösende Simulation.</span><span class="sxs-lookup"><span data-stu-id="be317-116">High resolution simulation.</span></span> <span data-ttu-id="be317-117">In der Simulation wird eine 1024 x 1024 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.</span><span class="sxs-lookup"><span data-stu-id="be317-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="be317-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="be317-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="be317-119">Simulation mit der höchsten Auflösung.</span><span class="sxs-lookup"><span data-stu-id="be317-119">Highest resolution simulation.</span></span> <span data-ttu-id="be317-120">In der Simulation wird eine 2048 x 2048 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.</span><span class="sxs-lookup"><span data-stu-id="be317-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="be317-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ HighQuality**</span><span class="sxs-lookup"><span data-stu-id="be317-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="be317-122">Die Simulation ist unabhängig von der ausgewählten Auflösung mit hoher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="be317-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="be317-123">Durch Festlegen dieses Werts wird das Rauschen der Ergebnisse der direkt Beleuchtungs Simulation reduziert, obwohl die Simulation langsamer verläuft.</span><span class="sxs-lookup"><span data-stu-id="be317-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="be317-124">Kann mit einem der Auflösungswerte kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="be317-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="be317-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="be317-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="be317-126">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="be317-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="be317-127">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="be317-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="be317-128">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="be317-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be317-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be317-129">Remarks</span></span>

<span data-ttu-id="be317-130">Es kann nur einer der Auflösungswerte angegeben werden, der mit dem hochwertigen Wert kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="be317-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be317-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be317-131">Requirements</span></span>



| <span data-ttu-id="be317-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be317-132">Requirement</span></span> | <span data-ttu-id="be317-133">Wert</span><span class="sxs-lookup"><span data-stu-id="be317-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be317-134">Header</span><span class="sxs-lookup"><span data-stu-id="be317-134">Header</span></span><br/> | <dl> <span data-ttu-id="be317-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="be317-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be317-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be317-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be317-137">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="be317-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




