---
title: D3DX11_PASS_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Durchlauf, der den Pipeline Zustand enthält.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982549"
---
# <a name="d3dx11_pass_desc-structure"></a>Bibliothek d3dx11 \_ Pass- \_ de-Struktur

Beschreibt einen Effekt Durchlauf, der den Pipeline Zustand enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der Name dieses Pass (**null** , wenn nicht anonym).

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen zu diesem Durchlauf.

</dd> <dt>

**piainputsignature**
</dt> <dd>

Type: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Signatur aus dem Scheitelpunkt-Shader oder Geometry-Shader (wenn kein Scheitelpunkt-Shader vorhanden ist) oder **null** , wenn keines vorhanden ist.

</dd> <dt>

**Iainputsignaturesize**
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Größe der Größe in Bytes.

</dd> <dt>

**Schablone Ref**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der im Status der tiefen Schablone verwendete Schablonen Verweis Wert.

</dd> <dt>

**Samplemask**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Beispiel Maske für den Blend-Zustand.

</dd> <dt>

**Blendfactor**
</dt> <dd>

Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die pro-Komponente-Blend-Faktoren (RGBA) für den Blend-Zustand.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bibliothek d3dx11 \_ Pass-Debug \_ wird mit [**ID3DX11EffectPass:: getdebug**](id3dx11effectpass-getdesc.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

