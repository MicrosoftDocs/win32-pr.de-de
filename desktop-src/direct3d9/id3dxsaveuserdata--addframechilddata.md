---
description: Fügen Sie dem Frame untergeordnete Daten hinzu.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: ID3DXSaveUserData::AddFrameChildData-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0b593010ec9ff8a56833c48b9667dfd0084f99283fc4bf29c9008e9e31ac98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095720"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a>ID3DXSaveUserData::AddFrameChildData-Methode

Fügen Sie dem Frame untergeordnete Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFrame* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFRAME**](d3dxframe.md) \***

Zeiger auf einen Meshcontainer. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofSave* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein .x-Datei-Speicherobjekt. Verwenden Sie den Zeiger zum Aufrufen von [**ID3DXFileSaveObject::AddDataObject,**](id3dxfilesaveobject--adddataobject.md) um ein untergeordnetes Datenobjekt hinzuzufügen. Speichern Sie die Daten nicht mit [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).

</dd> <dt>

*pXofFrameData* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**

Zeiger auf einen .x-Dateidatenknoten. Verwenden Sie den Zeiger zum Aufrufen von [**ID3DXFileSaveData::AddDataObject,**](id3dxfilesavedata--adddataobject.md) um ein untergeordnetes Datenobjekt hinzuzufügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückgegeben wird, da dadurch [**auch D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="remarks"></a>Hinweise

[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) und [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer X-Datei zum Speichern von Benutzerdaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
