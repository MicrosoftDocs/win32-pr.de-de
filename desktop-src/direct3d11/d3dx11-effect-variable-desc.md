---
title: D3DX11_EFFECT_VARIABLE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Variable.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996203"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>Bibliothek d3dx11 Effect-Variablen (Debug- \_ \_ \_ Struktur)

Beschreibt eine Effekt Variable.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der Name dieser Variablen-, Annotation-oder Strukturmember.

</dd> <dt>

**Tischer**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die semantische Zeichenfolge dieses Variablen-oder Strukturmembers (null für Anmerkungen oder, wenn nicht vorhanden).

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Optionale Flags für Effekt Variablen.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen für diese Variable (immer 0 für Anmerkungen).

</dd> <dt>

**BufferOffset**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Offset in enthaltende cBuffer oder tBuffer (immer 0 für Anmerkungen oder Variablen, die nicht in konstantenpuffern enthalten sind).

</dd> <dt>

**Explitbindpoint**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Wird verwendet, wenn die Variable mithilfe des Register-Schlüssel Worts explizit gebunden wurde. Häkchen für \_ den \_ \_ expliziten \_ Bindungspunkt der Bibliothek d3dx11 Effect-Variable \_ .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die \_ Variable "Bibliothek d3dx11 Effect" \_ \_ wird mit " [**ID3DX11EffectVariable:: getdebug**](id3dx11effectvariable-getdesc.md)" verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

