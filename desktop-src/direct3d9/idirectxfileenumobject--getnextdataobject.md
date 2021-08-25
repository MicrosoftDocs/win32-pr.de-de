---
description: Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: IDirectXFileEnumObject::GetNextDataObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 42d95fcee1b431f5121389d7bb6595e5c53ca56298c75ed6010ee86733c310e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985130"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>IDirectXFileEnumObject::GetNextDataObject-Methode

Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse eines Zeigers auf eine [**IDirectXFileData-Schnittstelle,**](idirectxfiledata.md) die das zurückgegebene Dateidatenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>Hinweise

Objekte der obersten Ebene sind immer Datenobjekte. Datenverweisobjekte und binäre Objekte können nur untergeordnete Elemente von Datenobjekten sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




