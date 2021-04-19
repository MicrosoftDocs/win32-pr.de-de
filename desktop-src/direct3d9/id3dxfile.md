---
description: Anwendungen verwenden die Methoden der ID3DXFile-Schnittstelle, um Instanzen der ID3DXFileEnumObject-und ID3DXFileSaveObject-Schnittstellen zu erstellen und um Vorlagen zu registrieren.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: ID3DXFile-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361219"
---
# <a name="id3dxfile-interface"></a>ID3DXFile-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFile-Schnittstelle, um Instanzen der [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -und [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstellen zu erstellen und um Vorlagen zu registrieren.

## <a name="members"></a>Member

Die **ID3DXFile** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFile** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**"Kreateendumuject"**](id3dxfile--createenumobject.md)           | Erstellt ein Enumeratorobjekt, das eine x-Datei liest.<br/>                                                      |
| [**"Kreatesaveobject"**](id3dxfile--createsaveobject.md)           | Erstellt ein Speicher Objekt, das zum Speichern von Daten in einer x-Datei verwendet wird.<br/>                                          |
| [**Registerenumtemplates**](id3dxfile--registerenumtemplates.md) | Registriert benutzerdefinierte Vorlagen bei Angabe eines [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt.<br/> |
| [**Register Templates**](id3dxfile--registertemplates.md)         | Registriert benutzerdefinierte Vorlagen.<br/>                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Ein ID3DXFile-Objekt enthält auch einen lokalen Vorlagen Speicher. Dieser lokale Speicher kann nur mit den Methoden [**ID3DXFile:: registerenumtemplates**](id3dxfile--registerenumtemplates.md) und [**ID3DXFile:: registertemplates**](id3dxfile--registertemplates.md) hinzugefügt werden.

[**ID3DXFileEnumObject**](id3dxfileenumobject.md) -und [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Objekte, die mit [**ID3DXFile:: anateenumubject**](id3dxfile--createenumobject.md) und [**ID3DXFile:: anatesaveobject**](id3dxfile--createsaveobject.md) erstellt wurden, nutzen auch den Vorlagen Speicher des übergeordneten ID3DXFile-Objekts.

Die ID3DXFile-Schnittstelle wird durch Aufrufen der [**D3DXFileCreate**](d3dxfilecreate.md) -Funktion abgerufen.

Die Globally Unique Identifier (GUID) für die ID3DXFile-Schnittstelle ist IID \_ ID3DXFile.

Der LPD3DXFILE-Typ wird als Zeiger auf die ID3DXFile-Schnittstelle definiert.


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Datei Schnittstellen](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
