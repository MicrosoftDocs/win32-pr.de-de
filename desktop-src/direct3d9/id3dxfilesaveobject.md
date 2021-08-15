---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine X-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: ID3DXFileSaveObject-Schnittstelle (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6efb87f92a81ec40fe919d76d18a9746e0d88c45f19616933f1b014402aa3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121184"
---
# <a name="id3dxfilesaveobject-interface"></a>ID3DXFileSaveObject-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine X-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.

## <a name="members"></a>Member

Die **ID3DXFileSaveObject-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileSaveObject** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileSaveObject-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData-Objekts**](id3dxfilesavedata.md) hinzu.<br/>                       |
| [**Getfile**](id3dxfilesaveobject--getfile.md)             | Ruft die [**ID3DXFile-Schnittstelle**](id3dxfile.md) des Objekts ab, das dieses **ID3DXFileSaveObject-Objekt erstellt** hat.<br/> |
| [**Speichern**](id3dxfilesaveobject--save.md)                   | Speichert ein Datenobjekt und seine unteren Daten in einer X-Datei auf dem Datenträger.<br/>                                                        |



 

## <a name="remarks"></a>Hinweise

Vorlagen sind nicht in jeder Datei erforderlich. Beispielsweise könnten Sie alle Vorlagen in einer einzelnen X-Datei speichern, anstatt sie in jeder X-Datei zu duplizieren.

Die ID3DXFileSaveObject-Schnittstelle wird durch Aufrufen der [**ID3DXFile::CreateSaveObject-Methode**](id3dxfile--createsaveobject.md) ermittelt.

Die GUID (Globally Unique Identifier) für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.

Der LPD3DXFILESAVEOBJECT-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX X-Dateischnittstellen](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
