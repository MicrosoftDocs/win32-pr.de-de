---
description: Anwendungen verwenden die Methoden der IDirectXFile-Schnittstelle, um Instanzen der Schnittstellen IDirectXFileEnumObject und IDirectXFileSaveObject zu erstellen und Vorlagen zu registrieren. Veraltet.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: IDirectXFile-Schnittstelle (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 7b2a6094b1c07a29ef354c37fe0bc8537b001dc97db95f75f3b492e2e33f2bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093502"
---
# <a name="idirectxfile-interface"></a>IDirectXFile-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFile-Schnittstelle, um Instanzen der Schnittstellen [**IDirectXFileEnumObject**](idirectxfileenumobject.md) und [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) zu erstellen und Vorlagen zu registrieren. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFile-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFile** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFile-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**CreateEnumObject**](idirectxfile--createenumobject.md)   | Erstellt ein Enumeratorobjekt. Veraltet.<br/> |
| [**CreateSaveObject**](idirectxfile--createsaveobject.md)   | Erstellt ein Speicherobjekt. Veraltet.<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | Registriert benutzerdefinierte Vorlagen. Veraltet.<br/>   |



 

## <a name="remarks"></a>Hinweise

Die GUID (Globally Unique Identifier) für die IDirectXFile-Schnittstelle ist IID \_ IDirectXFile.

Die IDirectXFile-Schnittstelle wird durch Aufrufen der [**DirectXFileCreate-Funktion**](directxfilecreate.md) abgerufen.

Der LPDIRECTXFILE-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Dateischnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
