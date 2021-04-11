---
description: Fügen Sie dem Mesh untergeordnete Daten hinzu.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'ID3DXSaveUserData:: addmeshchilddata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219685"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>ID3DXSaveUserData:: addmeshchilddata-Methode

Fügen Sie dem Mesh untergeordnete Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmeshcontainer* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Zeiger auf einen Mesh-Container. Siehe [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pxofsave* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein x-Dateispeicher Objekt. Verwenden Sie den Zeiger, um [**ID3DXFileSaveObject:: adddataobject**](id3dxfilesaveobject--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen. Speichern Sie die Daten nicht mit [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pxofmeshdata* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Zeiger auf einen x-Datei Datenknoten. Verwenden Sie den Zeiger, um [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen.

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

 

 
