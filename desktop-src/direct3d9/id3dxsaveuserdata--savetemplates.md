---
description: Ein Rückruf für den Benutzer zum Speichern einer X-Dateivorlage.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: ID3DXSaveUserData::SaveTemplates-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00695f11f267c77838bc2d9a3d2932df108c7323f3751b385c009abe2b21f540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293108"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a>ID3DXSaveUserData::SaveTemplates-Methode

Ein Rückruf für den Benutzer zum Speichern einer X-Dateivorlage.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pXofSave* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Zeiger auf ein .x-Datei-Speicherobjekt. Verwenden Sie diesen Parameter nicht, um Datenobjekte hinzuzufügen. Siehe [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückgegeben wird, da dadurch auch [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="remarks"></a>Hinweise

[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) und **ID3DXSaveUserData::SaveTemplates** bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer X-Datei zum Speichern von Benutzerdaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
