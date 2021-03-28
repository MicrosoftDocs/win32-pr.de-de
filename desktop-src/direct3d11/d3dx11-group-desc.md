---
title: D3DX11_GROUP_DESC-Struktur (D3dx11effect. h)
description: Beschreibt eine Effekt Gruppe.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050938"
---
# <a name="d3dx11_group_desc-structure"></a>Struktur der Bibliothek d3dx11- \_ Gruppe \_

Beschreibt eine Effekt Gruppe.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der Name dieser Gruppe (nur **null** , wenn Global).

</dd> <dt>

**O**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der in der Gruppe enthaltenen Techniken.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen in dieser Gruppe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Bibliothek d3dx11- \_ Gruppe muss \_ mit [**ID3DX11EffectTechnique:: getdebug**](id3dx11effecttechnique-getdesc.md)verwendet werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effekte 11-Strukturen](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

