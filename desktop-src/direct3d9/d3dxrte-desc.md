---
description: Beschreibt ein von einer Instanz von ID3DXRenderToEnvMap verwendetes Renderziel von einem Bildschirm.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: D3DXRTE_DESC-Struktur (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219501"
---
# <a name="d3dxrte_desc-structure"></a>D3DXRTE- \_ Struktur

Beschreibt ein von einer Instanz von [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)verwendetes Renderziel von einem Bildschirm.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite und Höhe in Pixel.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Maximale Detailebene (LOD).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Farb Puffer Format.

</dd> <dt>

**Depthstencil**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Gibt an, ob der z-Puffer benötigt wird.

</dd> <dt>

**Depthstencilformat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Das Format des tiefen Puffers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zum Zurückgeben der Erstellungs Parameter verwendet, die beim Erstellen eines [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) -Objekts verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
