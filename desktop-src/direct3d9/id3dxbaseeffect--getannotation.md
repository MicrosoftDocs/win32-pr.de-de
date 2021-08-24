---
description: Ruft das Handle einer Anmerkung ab.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: ID3DXBaseEffect::GetAnnotation-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c35deeb04e7cf21be429976c102fdf7c3126b1691b3f63725fc994ef79f7ad42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279010"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>ID3DXBaseEffect::GetAnnotation-Methode

Ruft das Handle einer Anmerkung ab.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hObject* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle einer Technik, eines Übergebens oder eines Parameters der obersten Ebene. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anmerkungsindex.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Anmerkung oder **NULL zurück,** wenn der Index ungültig war. Siehe [Handles (Direct3D 9).](handles.md)

## <a name="remarks"></a>Hinweise

Anmerkungen sind benutzerspezifische Daten, die an beliebige Verfahren, Übergeben oder Parameter angefügt werden können. Siehe [Handles (Direct3D 9).](handles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
