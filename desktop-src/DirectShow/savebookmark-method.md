---
description: Die SaveBookmark-Methode speichert die aktuelle Datenträgerposition und den aktuellen Status des MSWebDVD-Objekts, damit der Benutzer später an denselben Ort zurückkehren kann.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: SaveBookmark-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072714"
---
# <a name="savebookmark-method"></a>SaveBookmark-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Methode speichert die aktuelle Datenträgerposition und den aktuellen Status des `SaveBookmark` **MSWebDVD-Objekts,** damit der Benutzer später an denselben Ort zurückkehren kann.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Ein Lesezeichen ist eine Momentaufnahme des aktuellen Status des DVD-Navigators. Dies schließt Informationen ein, z. B., wo sie auf dem Datenträger abspielt und welche Audio- und Unterbildstreams ausgewählt sind. Durch speichern eines Lesezeichens kann der Benutzer die Anwendung schließen, den Computer herunterfahren und später wiederkommen, um die Anzeige des Datenträgers an der Stelle, an der er aufgelassen hat, mit allen Einstellungen wie zuvor fortsetzen. Es kann immer nur ein Lesezeichen gespeichert werden. Wenn Sie `SaveBookmark` aufrufen, wird das alte Lesezeichen überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




