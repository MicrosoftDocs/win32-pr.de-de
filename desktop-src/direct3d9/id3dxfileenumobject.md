---
description: Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Datei Datenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: ID3DXFileEnumObject-Schnittstelle (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961657"
---
# <a name="id3dxfileenumobject-interface"></a>ID3DXFileEnumObject-Schnittstelle

Anwendungen verwenden die Methoden der ID3DXFileEnumObject-Schnittstelle, um die untergeordneten Datei Datenobjekte in der Datei zu durchlaufen und ein untergeordnetes Objekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen.

## <a name="members"></a>Member

Die **ID3DXFileEnumObject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXFileEnumObject** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXFileEnumObject** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Ruft ein untergeordnetes-Objekt in diesem Datei Datenobjekt ab.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Ruft die Anzahl der untergeordneten Objekte in diesem Datei Datenobjekt ab.<br/> |
| [**Getdataobjectbyid**](id3dxfileenumobject--getdataobjectbyid.md)     | Ruft das Datenobjekt ab, das über die angegebene GUID verfügt.<br/>          |
| [**Getdataobjectbyname**](id3dxfileenumobject--getdataobjectbyname.md) | Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Ruft das [**ID3DXFile**](id3dxfile.md) -Objekt ab.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die ID3DXFileEnumObject-Schnittstelle ist IID \_ ID3DXFileEnumObject.

Der LPD3DXFILEENUMOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
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

 

 
