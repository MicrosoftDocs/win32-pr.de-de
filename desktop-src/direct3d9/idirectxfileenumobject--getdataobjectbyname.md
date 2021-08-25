---
description: Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt. Veraltet.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: IDirectXFileEnumObject::GetDataObjectByName-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 0b5498833096a673226af60188397fb518f483b26d6b470021c590e16d190342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893200"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a>IDirectXFileEnumObject::GetDataObjectByName-Methode

Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den angeforderten Namen.

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

 

 
