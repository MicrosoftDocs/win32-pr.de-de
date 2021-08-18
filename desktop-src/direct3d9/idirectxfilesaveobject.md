---
description: Anwendungen verwenden die Methoden der IDirectXFileSaveObject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: IDirectXFileSaveObject-Schnittstelle (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 7274ca544d7164400fc528fdec6f9640647126989637aa75929a3a9ae1cb72ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846900"
---
# <a name="idirectxfilesaveobject-interface"></a>IDirectXFileSaveObject-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFileSaveObject-Schnittstelle, um Datenobjekte zu erstellen und Vorlagen und Datenobjekte zu speichern. Beachten Sie, dass Vorlagen nicht in jeder Datei erforderlich sind. Beispielsweise könnten Sie alle Vorlagen in einer einzelnen Microsoft DirectX-Datei speichern, anstatt sie in jeder DirectX-Datei zu duplizieren. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFileSaveObject-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileSaveObject** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFileSaveObject-Schnittstelle** verfügt über diese Methoden.



| Methode                                                               | Beschreibung                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Createdataobject**](idirectxfilesaveobject--createdataobject.md) | Erstellt ein Datenobjekt. Veraltet.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Speichert ein Datenobjekt und seine unteren Daten in einer DirectX-Datei. Veraltet.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Speichert Vorlagen in einer DirectX-Datei. Veraltet.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Die GUID (Globally Unique Identifier) für die IDirectXFileSaveObject-Schnittstelle ist **IID \_ IDirectXFileSaveObject.**

Die **IDirectXFileSaveObject-Schnittstelle** wird durch Aufrufen der [**IDirectXFile::CreateSaveObject-Methode**](idirectxfile--createsaveobject.md) ermittelt.

Der **LPDIRECTXFILESAVEOBJECT-Typ** wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[X-Dateischnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
