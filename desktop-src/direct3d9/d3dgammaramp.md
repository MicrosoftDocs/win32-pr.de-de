---
description: Enthält Daten zu roten, grünen und blauen Rampen.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: D3DGAMMARAMP-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fbd3acc35b7fd4998f5ba536c1fe4a28cf2a17153bf24aacde1f9f39bbbcd09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751000"
---
# <a name="d3dgammaramp-structure"></a>D3DGAMMARAMP-Struktur

Enthält Daten zu roten, grünen und blauen Rampen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Member

<dl> <dt>

**Rot**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array mit 256 WORD-Elementen, das die rote Gamma-Rampe beschreibt.

</dd> <dt>

**Grün**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array mit 256 WORD-Elementen, das die grüne Gammaverlauf beschreibt.

</dd> <dt>

**Blau**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array mit 256 WORD-Elementen, das die blaue Gamma-Rampe beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
