---
description: Anwendungen verwenden die Methoden der IDirectXFileBinary-Schnittstelle, um Informationen zu Binärdaten zu lesen und abzurufen. Veraltet.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: IDirectXFileBinary-Schnittstelle (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 46e0da3a0cb03d3769e7888706a48fbf00786471afed285ce54c629285ac158c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292409"
---
# <a name="idirectxfilebinary-interface"></a>IDirectXFileBinary-Schnittstelle

Anwendungen verwenden die Methoden der IDirectXFileBinary-Schnittstelle, um Informationen zu Binärdaten zu lesen und abzurufen. Veraltet.

## <a name="members"></a>Member

Die **IDirectXFileBinary-Schnittstelle** erbt von [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDirectXFileBinary-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Ruft den mime Multipurpose Internet Mail Extensions typ (MIME) für die Binärdaten ab. Veraltet.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Ruft die Größe der Binärdaten ab. Veraltet.<br/>                                               |
| [**Lesen**](idirectxfilebinary--read.md)               | Liest die Binärdaten. Veraltet.<br/>                                                               |



 

## <a name="remarks"></a>Hinweise

Die GUID für die IDirectXFileBinary-Schnittstelle ist IID \_ IDirectXFileBinary.

Der LPDIRECTXFileBinary-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X-Dateischnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




