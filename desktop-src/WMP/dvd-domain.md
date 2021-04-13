---
title: DVD. Domäne
description: Die Domänen Eigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. Domänen-Windows-Media Player
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
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340597"
---
# <a name="dvddomain"></a>DVD. Domäne

Die **Domänen** Eigenschaft ruft die aktuelle Domäne der DVD ab.

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die einen der folgenden Werte enthält.



| Zeichenfolge            | Beschreibung                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| FirstPlay         | Die Standard Initialisierung einer DVD-CD wird durchgeführt.                                                                                      |
| videomanagermenu  | Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "topmenu" für Windows-Media Player bezeichnet. Wird üblicherweise als Titelmenü oder im oberen Menü bezeichnet. |
| videotitlesetmenu | Anzeigen von Menüs für den aktuellen Titel Satz. Wird auch als titlemenu für Windows-Media Player bezeichnet. Wird üblicherweise als Stamm Menü bezeichnet.              |
| title             | Normalerweise wird der aktuelle Titel angezeigt.                                                                                                 |
| stop              | Der DVD-Navigator befindet sich in der DVD-stoppdomäne.                                                                                          |
| nicht definiert         | Der Player befindet sich nicht in einer DVD-Domäne.                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Einige DVDs enthalten nicht die Domänen FirstPlay, videomanagermenu oder videotitlesetmenu.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer eine leere Zeichenfolge zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





