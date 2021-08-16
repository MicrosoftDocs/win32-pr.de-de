---
description: Ruft das ID3DXFile-Objekt ab.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: ID3DXFileEnumObject::GetFile-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b07874cf492bc84207c6ea084df4c8a7506e1a6b3fdf6f94947092ad13cd160d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802732"
---
# <a name="id3dxfileenumobjectgetfile-method"></a>ID3DXFileEnumObject::GetFile-Methode

Ruft das [**ID3DXFile-Objekt**](id3dxfile.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppFile* \[ out\]
</dt> <dd>

Typ: **[ **ID3DXFile**](id3dxfile.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFile-Schnittstelle,**](id3dxfile.md) die das zurückgegebene Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 




