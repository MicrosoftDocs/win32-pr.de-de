---
description: Beschreibt eine von einem Effekt verwendete Technik.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC -Struktur (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 7e835c0eac067825942568464df8d5d345a06b530b71b7eaf7f319eae5f5d366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630730"
---
# <a name="d3dxtechnique_desc-structure"></a>D3DXTECHNIQUE \_ DESC-Struktur

Beschreibt eine von einem Effekt verwendete Technik.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine Zeichenfolge, die den Techniknamen enthält.

</dd> <dt>

**Übergibt**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Renderingüberläufen, die für die Technik erforderlich sind. Siehe Hinweise.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl der Anmerkungen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit \_ Anmerkungen.](using-an-effect.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Einige Grafikkarten können zwei Texturen in einem einzelnen Durchgang rendern. Wenn eine Karte jedoch nicht über diese Funktion verfügt, ist es häufig möglich, den gleichen Effekt in zwei Durchläufen zu rendern, indem sie eine Textur für jeden Durchgang verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
