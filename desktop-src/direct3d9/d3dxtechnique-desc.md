---
description: Beschreibt ein von einem Effekt verwendetes Verfahren.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC-Struktur (D3dx9effect. h)
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
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050846"
---
# <a name="d3dxtechnique_desc-structure"></a>D3DXTECHNIQUE- \_ Struktur

Beschreibt ein von einem Effekt verwendetes Verfahren.

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

Eine Zeichenfolge, die den Namen der Technik enthält.

</dd> <dt>

**Ausweisen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl von Renderingdurchläufen, die für das Siehe Hinweise.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl der Anmerkungen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Einige Grafikkarten können zwei Texturen in einem einzigen Durchlauf renderingzeichen darstellen. Wenn eine Karte jedoch nicht über diese Funktion verfügt, ist es oft möglich, denselben Effekt in zwei Durchläufen zu rendern, wobei eine Textur für jeden Durchlauf verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
