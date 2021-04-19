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
# <a name="d3dxshgpusimopt-enumeration"></a>D3DXSHGPUSIMOPT-Enumeration

Beschreibt die Auflösung des Schatten-z-Puffers, der in der direkt Beleuchtungs Simulation der vorab berechneten Strahlen Übertragung (PRT) auf der GPU verwendet wird. Ein z-Puffer mit höherer Qualität kann auch angegeben werden, um das Rauschen der Ergebnisse der direkt Beleuchtungs Simulation zu reduzieren, obwohl die Simulation langsamer ist.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**
</dt> <dd>

Simulation mit niedriger Auflösung. In der Simulation wird eine 256 x 256 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**
</dt> <dd>

Simulation mit mittlerer Auflösung. In der Simulation wird eine 512 x 512 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet. Dies ist der Standardwert.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**
</dt> <dd>

Hochauflösende Simulation. In der Simulation wird eine 1024 x 1024 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**
</dt> <dd>

Simulation mit der höchsten Auflösung. In der Simulation wird eine 2048 x 2048 Pixel Textur zum Codieren des Schatten-z-Puffers verwendet.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ HighQuality**
</dt> <dd>

Die Simulation ist unabhängig von der ausgewählten Auflösung mit hoher Genauigkeit. Durch Festlegen dieses Werts wird das Rauschen der Ergebnisse der direkt Beleuchtungs Simulation reduziert, obwohl die Simulation langsamer verläuft. Kann mit einem der Auflösungswerte kombiniert werden.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es kann nur einer der Auflösungswerte angegeben werden, der mit dem hochwertigen Wert kombiniert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




