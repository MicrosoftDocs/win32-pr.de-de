---
title: D3DX11_TECHNIQUE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Technik.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762180"
---
# <a name="d3dx11_technique_desc-structure"></a>Bibliothek d3dx11 \_ Technique- \_ Struktur

Beschreibt eine Effekt Technik.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der Name dieser Technik (null, wenn nicht anonym).

</dd> <dt>

**Ausweisen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der in der Technik enthaltenen Übergänge.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen zu dieser Technik.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bibliothek d3dx11 \_ Technique \_ wird mit [**ID3DX11EffectTechnique:: getdebug**](id3dx11effecttechnique-getdesc.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

