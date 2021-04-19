---
description: Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'ID3DXSaveUserData:: registertemplates-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355837"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>ID3DXSaveUserData:: registertemplates-Methode

Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxfileapi* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFILE**](id3dxfile.md)**

Verwenden Sie diesen Zeiger, um benutzerdefinierte x-Datei Vorlagen zu registrieren. Siehe [**ID3DXFile**](id3dxfile.md). Verwenden Sie diesen Parameter nicht zum Hinzufügen von Datenobjekten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.

## <a name="remarks"></a>Bemerkungen

**ID3DXSaveUserData:: registertemplates** und [**ID3DXSaveUserData:: savetemplates**](id3dxsaveuserdata--savetemplates.md) bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer x-Datei zum Speichern von Benutzerdaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
