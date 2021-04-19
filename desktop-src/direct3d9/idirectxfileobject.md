---
description: Anwendungen verwenden die Methoden der idirectxfileobject-Schnittstelle zum Abrufen von Informationen zu Microsoft DirectX-Datei Objekten. Veraltet.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Idirectxfileobject-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361859"
---
# <a name="idirectxfileobject-interface"></a>Idirectxfileobject-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfileobject-Schnittstelle zum Abrufen von Informationen zu Microsoft DirectX-Datei Objekten. Veraltet.

## <a name="members"></a>Member

Die **idirectxfileobject** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idirectxfileobject** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfileobject** -Schnittstelle verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird. Veraltet.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab. Veraltet.<br/>                   |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die idirectxfileobject-Schnittstelle ist IID \_ idirectxfileobject.

Der lpdirectxfileobject-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
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

 

 
