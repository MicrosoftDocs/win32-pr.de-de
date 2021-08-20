---
title: Ccollection.count
description: Die count-Eigenschaft ruft die Anzahl der verfügbaren CD- und DVD-Laufwerke auf dem System ab.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Ccollection.count-Windows Media Player
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db279f746640d09fac8b3852773afc27330fc9ca48d59a1470de7d42709e60f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864100"
---
# <a name="cdromcollectioncount"></a>Ccollection.count

Die **count-Eigenschaft** ruft die Anzahl der verfügbaren CD- und DVD-Laufwerke auf dem System ab.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

DVD-ROM-Laufwerke werden genau wie CD-Laufwerke gezählt. Das steuerelement Windows Media Player unterstützt jedoch nur DVD-Funktionen für Windows XP-Betriebssysteme oder höher. In der Regel können DVD-Laufwerke CD-Medien wieder geben, CD-Laufwerke jedoch keine DVD-Medien wieder.

**Windows Media Player 10 Mobile:** Diese Methode gibt immer 0 zurück.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *Ccollection verwendet.* **count,** um die Anzahl der auf dem Computer des Benutzers verfügbaren CD- und DVD-Laufwerke anzuzeigen. Das Player-Objekt wurde mit der ID = "Player" erstellt.


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





