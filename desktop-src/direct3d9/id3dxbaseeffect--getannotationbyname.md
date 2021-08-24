---
description: Ruft das Handle einer Anmerkung ab, indem deren Name gesucht wird.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: ID3DXBaseEffect::GetAnnotationByName-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a4a8943248ef2280bdb58c864a44c67a44a12c6f641fc05b74bb0fb28e2e9ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791060"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>ID3DXBaseEffect::GetAnnotationByName-Methode

Ruft das Handle einer Anmerkung ab, indem deren Name gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hObject* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle einer Technik, eines Durchlaufs oder eines Parameters der obersten Ebene. Siehe [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Anmerkungsnamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Anmerkung oder **NULL** zurück, wenn der Name nicht gefunden wurde. Siehe [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
