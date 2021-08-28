---
title: D3DX11_GROUP_DESC -Struktur (D3dx11effect.h)
description: Beschreibt eine Effektgruppe.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC-Struktur Direct3D 11
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
ms.openlocfilehash: a189417b997647fd9c48a55010e96b32053c64031a03a8ac845e48c9a8e870a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096310"
---
# <a name="d3dx11_group_desc-structure"></a>D3DX11 \_ GROUP \_ DESC-Struktur

Beschreibt eine Effektgruppe.

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

Name dieser Gruppe (nur **NULL,** wenn global).

</dd> <dt>

**Techniken**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der in der Gruppe enthaltenen Techniken.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen für diese Gruppe.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ GROUP \_ DESC wird mit [**ID3DX11EffectTechnique::GetDesc verwendet.**](id3dx11effecttechnique-getdesc.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

