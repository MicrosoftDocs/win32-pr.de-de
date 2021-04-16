---
description: Beschreibt einen Durchlauf für ein Effekt Objekt.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354147"
---
# <a name="d3dxpass_desc-structure"></a>D3DXPASS- \_ Struktur

Beschreibt einen Durchlauf für ein Effekt Objekt.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Der für den Durchlauf verwendete Zeichen folgen Wert.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).

</dd> <dt>

**pvertexshaderfunction**
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Zeiger auf die Vertex-Shader-Funktion. Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Struktur einen **null** -Zeiger zurück, wenn Sie von [**getpassde**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.

</dd> <dt>

**ppixelshaderfunction**
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Zeiger auf die Pixel-Shader-Funktion. Wenn ein Effekt mit [D3DXFX \_ Not \_ cloneable](d3dxfx.md)erstellt wird, gibt diese Struktur einen **null** -Zeiger zurück, wenn Sie von [**getpassde**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**Getpassde SC**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
