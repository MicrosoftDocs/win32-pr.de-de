---
description: Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine x-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: ID3DXFileSaveObject-Schnittstelle (D3DX9Xof. h)
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
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361200"
---
# <a name="id3dxfilesaveobject-interface"></a>ID3DXFileSaveObject-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileSaveObject-Schnittstelle, um eine x-Datei auf den Datenträger zu schreiben und Datenobjekte und Vorlagen hinzuzufügen und zu speichern.

## <a name="members"></a>Member

Die **ID3DXFileSaveObject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFileSaveObject** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileSaveObject** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Adddataobject**](id3dxfilesaveobject--adddataobject.md) | Fügt ein Datenobjekt als untergeordnetes Element des [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekts hinzu.<br/>                       |
| [**GetFile**](id3dxfilesaveobject--getfile.md)             | Ruft die [**ID3DXFile**](id3dxfile.md) -Schnittstelle des-Objekts ab, das dieses **ID3DXFileSaveObject** -Objekt erstellt hat.<br/> |
| [**Speichern**](id3dxfilesaveobject--save.md)                   | Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.<br/>                                                        |



 

## <a name="remarks"></a>Bemerkungen

In jeder Datei sind keine Vorlagen erforderlich. Beispielsweise können Sie alle Vorlagen in eine einzelne x-Datei einfügen, anstatt Sie in jeder. x-Datei zu duplizieren.

Die ID3DXFileSaveObject-Schnittstelle wird durch Aufrufen der [**ID3DXFile:: createsaveobject**](id3dxfile--createsaveobject.md) -Methode abgerufen.

Die Globally Unique Identifier (GUID) für die ID3DXFileSaveObject-Schnittstelle ist IID \_ ID3DXFileSaveObject.

Der LPD3DXFILESAVEOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
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

 

 
