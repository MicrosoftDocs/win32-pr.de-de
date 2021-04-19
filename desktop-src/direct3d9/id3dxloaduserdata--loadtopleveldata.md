---
description: Laden von Daten der obersten Ebene aus einer x-Datei.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'ID3DXLoadUserData:: loadtopleveldata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364003"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a>ID3DXLoadUserData:: loadtopleveldata-Methode

Laden von Daten der obersten Ebene aus einer x-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxofchilddata* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Zeiger auf eine x-Datei Datenstruktur. Dies wird in "dxfile. h" definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




