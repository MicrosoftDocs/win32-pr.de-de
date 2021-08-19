---
title: D3DX11_EFFECT_DESC -Struktur (D3dx11effect.h)
description: Beschreibt einen Effekt.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989990"
---
# <a name="d3dx11_effect_desc-structure"></a>D3DX11 \_ EFFECT \_ DESC-Struktur

Beschreibt einen Effekt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl konstanter Puffer in diesem Effekt.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der globalen Variablen in diesem Effekt.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der globalen Schnittstellen in diesem Effekt.

</dd> <dt>

**Techniken**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Techniken in diesem Effekt.

</dd> <dt>

**Gruppen**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Gruppen in diesem Effekt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ EFFECT \_ DESC wird mit [**ID3DX11Effect::GetDesc verwendet.**](id3dx11effect-getdesc.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

