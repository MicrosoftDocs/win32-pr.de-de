---
description: Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: ID3DXLoadUserData-Schnittstelle (D3dx9anim. h)
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
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373493"
---
# <a name="id3dxloaduserdata-interface"></a>ID3DXLoadUserData-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern. Eine Instanz dieser Schnittstelle wird an [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)und D3DX Ruft die entsprechende Methode für diese Schnittstelle immer dann auf, wenn die entsprechenden Daten gefunden werden. Beispielsweise wird für jedes Frame Objekt in der x-Datei [**ID3DXLoadUserData:: loadframechilddata**](id3dxloaduserdata--loadframechilddata.md) aufgerufen und die untergeordneten Daten übermittelt.

## <a name="members"></a>Member

Die **ID3DXLoadUserData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXLoadUserData** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXLoadUserData** -Schnittstelle verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**Loadframechilddata**](id3dxloaduserdata--loadframechilddata.md) | Laden von untergeordneten Frame-Daten aus einer x-Datei.<br/> |
| [**Loadmeshchilddata**](id3dxloaduserdata--loadmeshchilddata.md)   | Laden von untergeordneten Mesh-Daten aus einer x-Datei.<br/>  |
| [**Loadtopleveldata**](id3dxloaduserdata--loadtopleveldata.md)     | Laden von Daten der obersten Ebene aus einer x-Datei.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXLOADUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
