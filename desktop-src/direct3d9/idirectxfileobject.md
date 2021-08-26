---
description: Anwendungen verwenden die Methoden der IDirectXFileObject-Schnittstelle, um Informationen zu Microsoft DirectX-Dateiobjekten abzurufen. Veraltet.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: IDirectXFileObject-Schnittstelle (DXFile.h)
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
ms.openlocfilehash: 3aa0ffffb8766707841fa0a4a5ec54fe0db9caf1d86b885afc36bffa5f8352d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951300"
---
# <a name="idirectxfileobject-interface"></a>IDirectXFileObject-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFileObject-Schnittstelle, um Informationen zu Microsoft DirectX-Dateiobjekten abzurufen. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFileObject-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileObject** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFileObject-Schnittstelle** verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**Getid**](idirectxfileobject--getid.md)     | Ruft einen Zeiger auf die GUID ab, die ein DirectX-Dateiobjekt identifiziert. Veraltet.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Ruft einen Zeiger auf den Namen eines DirectX-Dateiobjekts ab. Veraltet.<br/>                   |



 

## <a name="remarks"></a>Hinweise

Die GUID für die IDirectXFileObject-Schnittstelle ist IID \_ IDirectXFileObject.

Der LPDIRECTXFILEOBJECT-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
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

 

 
