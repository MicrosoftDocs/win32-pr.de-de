---
description: Die ITablet3-Schnittstelle ermöglicht Multitouchabfragen für Eingaben.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: ITablet3-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449843"
---
# <a name="itablet3-interface"></a>ITablet3-Schnittstelle

Die ITablet3-Schnittstelle ermöglicht Multitouchabfragen für Eingaben.

## <a name="members"></a>Member

Die **ITablet3-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet3 verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITablet3-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Ruft die maximale Anzahl unterstützter Eingaben ab.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Gibt an, ob Multitouch für dieses Objekt aktiviert ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Entwickler sollten diese Schnittstelle nicht verwenden.

Der folgende Code beschreibt, wie die **ITablet3-Schnittstelle** definiert wird.

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

