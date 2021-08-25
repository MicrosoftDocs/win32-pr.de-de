---
description: Fügen Sie dem Gitternetz untergeordnete Daten hinzu.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: ID3DXSaveUserData::AddMeshChildData-Methode (D3dx9anim.h)
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
ms.openlocfilehash: 397dc9ade32222dd98e050110811464f6544a1d0af52729417c61fbc3367bdbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893310"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a>ID3DXSaveUserData::AddMeshChildData-Methode

Fügen Sie dem Gitternetz untergeordnete Daten hinzu.

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

*pMeshContainer* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***

Zeiger auf einen Gitternetzcontainer. Siehe [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> <dt>

*pXofSave* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein X-Dateispeicherobjekt. Verwenden Sie den Zeiger , um [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen. Speichern Sie die Daten nicht mit [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofMeshData* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Zeiger auf einen X-Dateidatenknoten. Verwenden Sie den Zeiger , um [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) aufzurufen, um ein untergeordnetes Datenobjekt hinzuzufügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode, um D3D \_ OK zurückzugeben. Programmieren Sie andernfalls die -Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**auch D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt, und den Fehler zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
