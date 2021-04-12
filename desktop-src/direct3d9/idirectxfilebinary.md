---
description: Anwendungen verwenden die Methoden der idirectxfilebinary-Schnittstelle zum Lesen und Abrufen von Informationen zu Binärdaten. Veraltet.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Idirectxfilebinary-Schnittstelle (dxfile. h)
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
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219476"
---
# <a name="idirectxfilebinary-interface"></a>Idirectxfilebinary-Schnittstelle

Anwendungen verwenden die Methoden der idirectxfilebinary-Schnittstelle zum Lesen und Abrufen von Informationen zu Binärdaten. Veraltet.

## <a name="members"></a>Member

Die **idirectxfilebinary** -Schnittstelle erbt von [**idirectxfileobject**](idirectxfileobject.md). **Idirectxfilebinary** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idirectxfilebinary** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Getmimetype**](idirectxfilebinary--getmimetype.md) | Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab. Veraltet.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Ruft die Größe der Binärdaten ab. Veraltet.<br/>                                               |
| [**Lesen**](idirectxfilebinary--read.md)               | Liest die Binärdaten. Veraltet.<br/>                                                               |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für die idirectxfilebinary-Schnittstelle ist IID \_ idirectxfilebinary.

Der lpdirectxfilebinary-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idirectxfileobject**](idirectxfileobject.md)
</dt> <dt>

[X-Datei Schnittstellen](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




