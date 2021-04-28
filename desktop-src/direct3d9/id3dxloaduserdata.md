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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093628"
---
# <a name="id3dxloaduserdata-interface"></a>ID3DXLoadUserData-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind. Eine Instanz dieser Schnittstelle wird [**an D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)übergeben, und D3DX ruft jedes Mal die entsprechende Methode auf dieser Schnittstelle auf, wenn die entsprechenden Daten gefunden werden. Beispielsweise wird für jedes Frameobjekt in der X-Datei [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) aufgerufen und die untergeordneten Daten übergeben.

## <a name="members"></a>Member

Die **ID3DXLoadUserData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLoadUserData** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXLoadUserData-Schnittstelle** verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Laden sie untergeordnete Framedaten aus einer X-Datei.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Laden von untergeordneten Meshdaten aus einer X-Datei.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Laden sie Daten der obersten Ebene aus einer X-Datei.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXLOADUSERDATA-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
