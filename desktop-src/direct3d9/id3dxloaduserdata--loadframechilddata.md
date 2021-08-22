---
description: Laden sie untergeordnete Framedaten aus einer X-Datei.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: ID3DXLoadUserData::LoadFrameChildData-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3dcb9fa8218804b0d6fdb5532dd54bc2b2b4a3921ea4462692a36e671efb404d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802180"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a>ID3DXLoadUserData::LoadFrameChildData-Methode

Laden sie untergeordnete Framedaten aus einer X-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFrame* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Zeiger auf einen Meshcontainer. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofChildData* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Zeiger auf eine X-Dateidatenstruktur. Dies wird in Dxfile.h definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückgegeben wird, da dadurch auch [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 




