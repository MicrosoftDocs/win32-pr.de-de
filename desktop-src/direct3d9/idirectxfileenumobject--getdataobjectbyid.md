---
description: Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: IDirectXFileEnumObject::GetDataObjectById-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 49bee0f513bcca71a98e72fb3f51e1bcc458083ce9b165b3e5163fb5f6b71708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292231"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a>IDirectXFileEnumObject::GetDataObjectById-Methode

Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
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

Typ: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**IDirectXFileData-Schnittstelle,**](idirectxfiledata.md) die das zurückgegebene Dateidatenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
