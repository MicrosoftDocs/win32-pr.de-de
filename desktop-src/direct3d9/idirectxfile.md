---
description: Anwendungen verwenden die Methoden der idirectxfile-Schnittstelle zum Erstellen von Instanzen der Schnittstellen idirectxfileenumubject und idirectxfilesaveobject und zum Registrieren von Vorlagen. Veraltet.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Idirectxfile-Schnittstelle (dxfile. h)
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
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870176"
---
# <a name="idirectxfile-interface"></a>Idirectxfile-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfile-Schnittstelle zum Erstellen von Instanzen der Schnittstellen [**idirectxfileenumubject**](idirectxfileenumobject.md) und [**idirectxfilesaveobject**](idirectxfilesaveobject.md) und zum Registrieren von Vorlagen. Veraltet.

## <a name="members"></a>Member

Die **idirectxfile** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idirectxfile** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**"Kreateendumuject"**](idirectxfile--createenumobject.md)   | Erstellt ein Enumeratorobjekt. Veraltet.<br/> |
| [**"Kreatesaveobject"**](idirectxfile--createsaveobject.md)   | Erstellt ein Save-Objekt. Veraltet.<br/>        |
| [**Register Templates**](idirectxfile--registertemplates.md) | Registriert benutzerdefinierte Vorlagen. Veraltet.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Der Globally Unique Identifier (GUID) für die idirectxfile-Schnittstelle ist IID \_ idirectxfile.

Die idirectxfile-Schnittstelle wird durch Aufrufen der [**directxfilecreate**](directxfilecreate.md) -Funktion abgerufen.

Der lpdirectxfile-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Datei Schnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
