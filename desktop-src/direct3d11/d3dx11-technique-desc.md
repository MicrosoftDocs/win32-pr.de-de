---
title: D3DX11_TECHNIQUE_DESC -Struktur (D3dx11effect.h)
description: Beschreibt eine Effekttechnik.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC-Struktur Direct3D 11
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
ms.openlocfilehash: 2266737a04b28940eeaa3758f5bd3909ec815745cb060836c499cfd4b3142266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124925"
---
# <a name="d3dx11_technique_desc-structure"></a>D3DX11 \_ TECHNIQUE \_ DESC-Struktur

Beschreibt eine Effekttechnik.

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

Name dieser Technik (NULL, wenn nicht anonym).

</dd> <dt>

**Übergibt**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der in der Technik enthaltenen Durchläufe.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen zu diesem Verfahren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ TECHNIQUE \_ DESC wird mit [**ID3DX11EffectTechnique::GetDesc verwendet.**](id3dx11effecttechnique-getdesc.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

