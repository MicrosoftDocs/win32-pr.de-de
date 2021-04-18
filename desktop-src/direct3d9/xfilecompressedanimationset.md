---
description: Identifiziert komprimierte Keyframe-Animationsdaten.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Xfilecompressedanimationset-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365075"
---
# <a name="xfilecompressedanimationset-structure"></a>Xfilecompressedanimationset-Struktur

Identifiziert komprimierte Keyframe-Animationsdaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Member

<dl> <dt>

**Compressedblocksize**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Gesamtgröße (in Bytes) der komprimierten Daten im komprimierten Keyframe-Animationsdaten Puffer.

</dd> <dt>

**Tickspersec**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Animations Tastatur-Frame Ticks, die pro Sekunde auftreten.

</dd> <dt>

**Playbacktyp**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Typ der Wiedergabe Schleife für Animations Sätze. Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Minimale Puffergröße in Bytes, die zum Speichern komprimierter Keyframe-Animationsdaten erforderlich ist. Der Wert ist gleich ((compressedblocksize + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateistrukturen](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
