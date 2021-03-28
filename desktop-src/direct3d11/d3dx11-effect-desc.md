---
title: D3DX11_EFFECT_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC Struktur Direct3D 11
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
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982588"
---
# <a name="d3dx11_effect_desc-structure"></a>Bibliothek d3dx11 \_ Effect- \_ Struktur Struktur

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

**Constantbuffers**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Konstanten Puffer in diesem Effekt.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der globalen Variablen in diesem Effekt.

</dd> <dt>

**Interfakevariables**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der globalen Schnittstellen in diesem Effekt.

</dd> <dt>

**O**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der in diesem Effekt beschriebenen Techniken.

</dd> <dt>

**Gruppen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Gruppen in diesem Effekt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

"Bibliothek d3dx11 Effect Debug" \_ \_ wird mit " [**ID3DX11Effect:: getdebug**](id3dx11effect-getdesc.md)" verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

