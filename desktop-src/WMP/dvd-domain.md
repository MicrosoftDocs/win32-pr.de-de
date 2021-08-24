---
title: DVD.domain
description: Die Domäneneigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD.domain Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0db8e6e212fec11de5f3619c2c1f97a90f579b34515983b0384d0d08ab0ff60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651170"
---
# <a name="dvddomain"></a>DVD.domain

Die **Domäneneigenschaft** ruft die aktuelle Domäne der DVD ab.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge,** die einen der folgenden Werte enthält.



| Zeichenfolge            | Beschreibung                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| firstPlay         | Ausführen der Standardinitialisierung eines DVD-Datenträgers.                                                                                      |
| videoManagerMenu  | Anzeigen von Menüs für den gesamten Datenträger. Wird auch als topMenu für Windows Media Player bezeichnet. Wird häufig als Titelmenü oder oberes Menü bezeichnet. |
| videoTitleSetMenu | Anzeigen von Menüs für den aktuellen Titelsatz. Wird auch als titleMenu für Windows Media Player bezeichnet. Wird häufig als Stammmenü bezeichnet.              |
| title             | In der Regel wird der aktuelle Titel angezeigt.                                                                                                 |
| stop              | Der DVD-Navigator befindet sich in der Domäne DVD-Beenden.                                                                                          |
| nicht definiert         | Der Player befindet sich in keiner DVD-Domäne.                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Jede DVD wird anders erstellt. Einige DVDs enthalten nicht die Domänen firstPlay, videoManagerMenu oder videoTitleSetMenu.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer eine leere Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





