---
title: Cdromcollection. Count
description: Die Count-Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Cdromcollection. count-Windows-Media Player
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
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371338"
---
# <a name="cdromcollectioncount"></a>Cdromcollection. Count

Die **count** -Eigenschaft ruft die Anzahl der verfügbaren CD-und DVD-Laufwerke im System ab.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

DVD-ROM-Laufwerke werden genau wie CD-Laufwerke gezählt. Das Windows Media Player-Steuerelement unterstützt jedoch nur DVD-Funktionen für Windows XP oder höhere Betriebssysteme. In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.

**Windows Media Player 10 Mobile:** Diese Methode gibt immer 0 (null) zurück.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **Anzahl, um** die Anzahl der CD-und DVD-Laufwerke anzuzeigen, die auf dem Computer des Benutzers verfügbar sind. Das Player-Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdromcollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





