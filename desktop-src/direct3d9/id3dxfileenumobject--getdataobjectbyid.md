---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: ID3DXFileEnumObject::GetDataObjectById-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a99da554a404a9bcc279830eaf50710a67a8c62bb61d1b67ac84c90b8fdc594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118660"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>ID3DXFileEnumObject::GetDataObjectById-Methode

Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rguid* \[ In\]
</dt> <dd>

Typ: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Verweis auf die angeforderte GUID.

</dd> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Adresse eines Zeigers auf eine [**ID3DXFileData-Schnittstelle,**](id3dxfiledata.md) die das zurückgegebene Dateidatenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="remarks"></a>Hinweise

Abrufen der GUID rguid des aktuellen Dateidatenobjekts mit der [**ID3DXFileData::GetId-Methode.**](id3dxfiledata--getid.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
