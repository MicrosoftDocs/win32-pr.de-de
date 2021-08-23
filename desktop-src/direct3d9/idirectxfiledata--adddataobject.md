---
description: Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: IDirectXFileData::AddDataObject-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491830"
---
# <a name="idirectxfiledataadddataobject-method"></a>IDirectXFileData::AddDataObject-Methode

Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataObj* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Zeiger auf eine [**IDirectXFileData-Schnittstelle,**](idirectxfiledata.md) die das Dateidatenobjekt darstellt, das als untergeordnetes Objekt hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**IDirectXFileSaveObject::CreateDataObject-Methode,**](idirectxfilesaveobject--createdataobject.md) um das [**IDirectXFileData-Objekt**](idirectxfiledata.md) zu erstellen, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




