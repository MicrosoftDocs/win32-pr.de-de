---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject:: getdataobjectbyid-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366664"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>ID3DXFileEnumObject:: getdataobjectbyid-Methode

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

*rguid* \[ in\]
</dt> <dd>

Typ: **[reguid](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Verweis auf die angeforderte GUID.

</dd> <dt>

*ppdataobj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Adresse eines Zeigers auf eine [**ID3DXFileData**](id3dxfiledata.md) -Schnittstelle, die das zurückgegebene Datei Datenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badvalue, dxfileerr \_ NotFound.

## <a name="remarks"></a>Bemerkungen

Rufen Sie die GUID-rguid des aktuellen Datei Datenobjekts mit der [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) -Methode ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
