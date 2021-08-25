---
description: 'ID3DXLoadUserData-Schnittstelle: Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.'
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: ID3DXLoadUserData-Schnittstelle (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ede66e7250a1dec095bd03a72ea69e58afb59a60b43647fd49adfc958689cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748120"
---
# <a name="id3dxloaduserdata-interface"></a>ID3DXLoadUserData-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind. Eine Instanz dieser Schnittstelle wird [**an D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)übergeben, und D3DX ruft jedes Mal die entsprechende Methode auf dieser Schnittstelle auf, wenn die entsprechenden Daten gefunden werden. Beispielsweise wird für jedes Frameobjekt in der X-Datei [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) aufgerufen und die untergeordneten Daten übergeben.

## <a name="members"></a>Member

Die **ID3DXLoadUserData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLoadUserData** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXLoadUserData-Schnittstelle** verfügt über diese Methoden.



| Methode                                                              | Beschreibung                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Laden sie untergeordnete Framedaten aus einer X-Datei.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Laden von untergeordneten Meshdaten aus einer X-Datei.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Laden sie Daten der obersten Ebene aus einer X-Datei.<br/>   |



 

## <a name="remarks"></a>Hinweise

Der LPD3DXLOADUSERDATA-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
