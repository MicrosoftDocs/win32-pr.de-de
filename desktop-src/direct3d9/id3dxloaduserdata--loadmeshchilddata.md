---
description: Laden von untergeordneten Meshdaten aus einer X-Datei.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: ID3DXLoadUserData::LoadMeshChildData-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd4aaa857ac89594b1114612c59f959f0d91b050f6f9c0f0c9290798acf829f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120824"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a>ID3DXLoadUserData::LoadMeshChildData-Methode

Laden von untergeordneten Meshdaten aus einer X-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshContainer* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Zeiger auf einen Meshcontainer. Siehe [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

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

 

 




