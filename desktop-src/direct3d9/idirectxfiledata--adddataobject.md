---
description: Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Idirectxfiledata:: adddataobject-Methode (dxfile. h)'
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
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355397"
---
# <a name="idirectxfiledataadddataobject-method"></a>Idirectxfiledata:: adddataobject-Methode

Fügt ein Datenobjekt als untergeordnetes Objekt hinzu. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdataobj* \[ in\]
</dt> <dd>

Typ: **[ **lpdirectxfiledata**](idirectxfiledata.md)**

Ein Zeiger auf eine [**idirectxfiledata**](idirectxfiledata.md) -Schnittstelle, die das Datei Datenobjekt darstellt, das als untergeordnetes Objekt hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ . Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**idirectxfilesaveobject:: createDataObject**](idirectxfilesaveobject--createdataobject.md) -Methode, um das [**idirectxfiledata**](idirectxfiledata.md) -Objekt zu erstellen, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idirectxfiledata](idirectxfiledata.md)
</dt> <dt>

[**Idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




