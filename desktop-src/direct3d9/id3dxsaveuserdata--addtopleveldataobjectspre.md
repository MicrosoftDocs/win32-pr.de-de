---
description: Fügen Sie vor der Framehierarchie ein Objekt der obersten Ebene hinzu.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: ID3DXSaveUserData::AddTopLevelDataObjectsPre-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52052a24c34c99260a68cd5cdeaa7487e6b71c086ac30922a06de241de8319ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801161"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a>ID3DXSaveUserData::AddTopLevelDataObjectsPre-Methode

Fügen Sie vor der Framehierarchie ein Objekt der obersten Ebene hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pXofSave* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein .x-Datei-Speicherobjekt. Verwenden Sie diesen Zeiger zum Aufrufen [**von IDirectXFileSaveObject::CreateDataObject,**](idirectxfilesaveobject--createdataobject.md) um das zu speichernde Datenobjekt zu erstellen. Rufen Sie dann [**IDirectXFileSaveObject::SaveData auf,**](idirectxfilesaveobject--savedata.md) um die Daten zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückgegeben wird, da dadurch auch [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
