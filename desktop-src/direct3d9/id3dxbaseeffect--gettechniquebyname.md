---
description: Ruft das Handle einer Technik ab, indem ihr Name gesucht wird.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: ID3DXBaseEffect::GetTechniqueByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 446c4625f6eee8c654991a9ed3685125e34d2de97553d328538deea0a7a4e116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121943"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>ID3DXBaseEffect::GetTechniqueByName-Methode

Ruft das Handle einer Technik ab, indem ihr Name gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Techniknamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der ersten Technik zurück, die über den angegebenen Namen verfügt, oder **NULL,** wenn der Name nicht gefunden wurde. Siehe [Handles (Direct3D 9).](handles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
