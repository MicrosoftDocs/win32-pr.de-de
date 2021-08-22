---
title: DVD.isAvailable
description: Die isAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann. | DVD.isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD.isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efb1a240c8df072d0770521f70c526f4e096c26385df85cff7acf0d229fdc252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996920"
---
# <a name="dvdisavailable"></a>DVD.isAvailable

Die **isAvailable-Eigenschaft** gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parameter

*name*

**Zeichenfolge,** die einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                            |
|------------|----------------------------------------------------------------------------------------|
| back (Zurück)       | Bestimmt, ob die **Back-Methode** verfügbar ist.                                   |
| Dvd        | Bestimmt, ob die DVD geladen wird.                                                  |
| dvdDecoder | Bestimmt, ob der DVD-Decoder auf dem System installiert ist.                             |
| resume     | Bestimmt, ob die **Resume-Methode** verfügbar ist.                                 |
| titleMenu  | Bestimmt, ob die **titleMenu-Methode** verfügbar ist.                              |
| topMenu    | Bestimmt, ob die **topMenu-Methode** verfügbar ist. Wird häufig als Stammmenü bezeichnet. |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen **schreibgeschützten booleschen Wert** zurück, der angibt, ob der angegebene Parameter verfügbar ist.

## <a name="remarks"></a>Hinweise

Die DVD-Features von Windows Media Player funktionieren nicht auf Computern, auf denen keine DVD-Decoder von Drittanbietern installiert sind. Sie können ermitteln, ob ein Decoder verfügbar ist, indem Sie **isAvailable** aufrufen ("dvdDecoder").

Jede DVD wird anders erstellt. Welche Methoden während der DVD-Wiedergabe und -Navigation verfügbar sind, hängt davon ab, wie die DVD erstellt wird.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





