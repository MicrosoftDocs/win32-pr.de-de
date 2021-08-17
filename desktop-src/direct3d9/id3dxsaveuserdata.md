---
description: 'ID3DXSaveUserData-Schnittstelle: Diese Schnittstelle wird von der Anwendung implementiert, um zusätzliche Benutzerdaten zu speichern, die in X-Dateien eingebettet sind.'
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: ID3DXSaveUserData-Schnittstelle (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5b0f02a4fb114f46930076f46ea7c416850a0e81f7369d4aab63a2de5ed6d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801136"
---
# <a name="id3dxsaveuserdata-interface"></a>ID3DXSaveUserData-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen Benutzerdaten zu speichern, die in X-Dateien eingebettet sind. Eine Instanz dieser Schnittstelle wird an [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)übergeben, und D3DX ruft jedes Mal die entsprechende Methode auf dieser Schnittstelle auf, wenn die entsprechenden Daten gefunden werden. Beispielsweise wird für jedes Frameobjekt in der X-Datei [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) aufgerufen und die untergeordneten Daten übergeben.

## <a name="members"></a>Member

Die **ID3DXSaveUserData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSaveUserData** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSaveUserData-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Fügen Sie dem Frame untergeordnete Daten hinzu.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Fügen Sie dem Gitternetz untergeordnete Daten hinzu.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Fügen Sie nach der Rahmenhierarchie ein Objekt der obersten Ebene hinzu.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Fügen Sie vor der Rahmenhierarchie ein Objekt der obersten Ebene hinzu.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Ein Rückruf für den Benutzer zum Registrieren einer X-Dateivorlage.<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | Ein Rückruf für den Benutzer zum Speichern einer X-Dateivorlage.<br/>     |



 

## <a name="remarks"></a>Hinweise

Der LPD3DXSAVEUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
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

 

 
