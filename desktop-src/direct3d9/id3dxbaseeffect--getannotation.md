---
description: Ruft das Handle einer Anmerkung ab.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect:: GetAnnotation-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364008"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>ID3DXBaseEffect:: GetAnnotation-Methode

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

*hobject* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle eines Verfahrens, eines bestanden oder eines Parameters der obersten Ebene. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Annotation-Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Anmerkung zurück, oder **null** , wenn der Index ungültig ist. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Bemerkungen

Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
