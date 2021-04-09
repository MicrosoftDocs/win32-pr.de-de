---
description: Fügen Sie ein Objekt der obersten Ebene nach der Frame Hierarchie hinzu.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: 'ID3DXSaveUserData:: addtopleveldataobjectspost-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPost
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3573bae8cbcb6858b04207f936545b7cf93959c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050930"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspost-method"></a>ID3DXSaveUserData:: addtopleveldataobjectspost-Methode

Fügen Sie ein Objekt der obersten Ebene nach der Frame Hierarchie hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxofsave* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein x-Dateispeicher Objekt. Verwenden Sie diesen Zeiger, um [**idirectxfilesaveobject:: kreatedataobject**](idirectxfilesaveobject--createdataobject.md) aufzurufen, um das zu speichernde Datenobjekt zu erstellen. Anschließend wird [**idirectxfilesaveobject:: SaveData**](idirectxfilesaveobject--savedata.md) aufgerufen, um die Daten zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
