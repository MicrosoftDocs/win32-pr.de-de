---
description: Anwendungen verwenden die Methoden der idirectxfileenumubject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen. Veraltet.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Idirectxfileendumubject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366454"
---
# <a name="idirectxfileenumobject-interface"></a>Idirectxfile-umubject-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfileenumubject-Schnittstelle, um die Datenobjekte in der Datei zu durchlaufen und ein Datenobjekt anhand seiner Globally Unique Identifier (GUID) oder anhand seines Namens abzurufen. Veraltet.

## <a name="members"></a>Member

Die **idirectxfileendumuject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idirectxfileenumubject** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfileerumuject** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Getdataobjectbyid**](idirectxfileenumobject--getdataobjectbyid.md)     | Ruft das Datenobjekt ab, das über die angegebene GUID verfügt. Veraltet.<br/>   |
| [**Getdataobjectbyname**](idirectxfileenumobject--getdataobjectbyname.md) | Ruft das Datenobjekt ab, das über den angegebenen Namen verfügt. Veraltet.<br/>   |
| [**Getnextdataobject**](idirectxfileenumobject--getnextdataobject.md)     | Ruft das nächste Objekt der obersten Ebene in der DirectX-Datei ab. Veraltet.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die idirectxfileeinumuject-Schnittstelle ist IID \_ idirectxfileeinumubject.

Der lpdirectxfileendumubject-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
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

 

 
