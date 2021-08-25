---
description: Beschreibt einen Durchlauf für ein Effektobjekt.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC-Struktur (D3dx9effect.h)
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
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894050"
---
# <a name="d3dxpass_desc-structure"></a>D3DXPASS \_ DESC-Struktur

Beschreibt einen Durchlauf für ein Effektobjekt.

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

Der für den Durchlauf verwendete Zeichenfolgenwert.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anmerkungen sind benutzerspezifische Daten, die an jede technik-, pass- oder parameter-Methode angefügt werden können. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit \_ Anmerkungen.](using-an-effect.md)

</dd> <dt>

**pVertexShaderFunction**
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Zeiger auf die Vertex-Shaderfunktion. Wenn ein Effekt mit [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)erstellt wird, gibt diese Struktur einen **NULL-Zeiger** zurück, wenn sie von [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.

</dd> <dt>

**pPixelShaderFunction**
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Zeiger auf die Pixelshaderfunktion. Wenn ein Effekt mit [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md)erstellt wird, gibt diese Struktur einen **NULL-Zeiger** zurück, wenn sie von [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)aufgerufen wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
