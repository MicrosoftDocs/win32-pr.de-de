---
description: Speichert ein Datenobjekt und seine children-Objekte in einer DirectX-Datei. Veraltet.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: IDirectXFileSaveObject::SaveData-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 293525d570540e00da4e8ac7680cf850b253c7e3ccbe3ffd152b639d0bc139cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747270"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a>IDirectXFileSaveObject::SaveData-Methode

Speichert ein Datenobjekt und seine children-Objekte in einer DirectX-Datei. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataObj* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Zeiger auf eine [**IDirectXFileData-Schnittstelle,**](idirectxfiledata.md) die das zu speichernde Dateidatenobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert DXFILE \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> </dl>

 

 




