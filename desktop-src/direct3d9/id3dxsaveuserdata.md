---
description: Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: ID3DXSaveUserData-Schnittstelle (D3dx9anim. h)
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
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350677"
---
# <a name="id3dxsaveuserdata-interface"></a>ID3DXSaveUserData-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um alle zusätzlichen in x-Dateien eingebetteten Benutzerdaten zu speichern. Eine Instanz dieser Schnittstelle wird an [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)und D3DX Ruft die entsprechende Methode für diese Schnittstelle immer dann auf, wenn die entsprechenden Daten gefunden werden. Beispielsweise wird für jedes Frame Objekt in der x-Datei [**ID3DXSaveUserData:: addframechilddata**](id3dxsaveuserdata--addframechilddata.md) aufgerufen und die untergeordneten Daten übermittelt.

## <a name="members"></a>Member

Die **ID3DXSaveUserData** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXSaveUserData** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXSaveUserData** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                              | BESCHREIBUNG                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**Addframechilddata**](id3dxsaveuserdata--addframechilddata.md)                   | Fügen Sie dem Frame untergeordnete Daten hinzu.<br/>                            |
| [**Addmeshchilddata**](id3dxsaveuserdata--addmeshchilddata.md)                     | Fügen Sie dem Mesh untergeordnete Daten hinzu.<br/>                             |
| [**Addtopleveldataobjectspost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Fügen Sie ein Objekt der obersten Ebene nach der Frame Hierarchie hinzu.<br/>       |
| [**Addtopleveldataobjectspre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Fügen Sie ein Objekt der obersten Ebene vor der Frame Hierarchie hinzu.<br/>      |
| [**Register Templates**](id3dxsaveuserdata--registertemplates.md)                   | Ein Rückruf für den Benutzer zum Registrieren einer x-Datei Vorlage.<br/> |
| [**Savetemplates**](id3dxsaveuserdata--savetemplates.md)                           | Ein Rückruf für den Benutzer zum Speichern einer x-Datei Vorlage.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXSAVEUSERDATA-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
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

 

 
