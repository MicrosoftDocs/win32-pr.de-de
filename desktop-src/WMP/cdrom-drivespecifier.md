---
title: Cdrom. drivespecifier
description: Die drivespecifier-Eigenschaft ruft den CD-oder DVD-Laufwerk Buchstaben ab.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Cdrom. drivespecifier-Fenster Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517522"
---
# <a name="cdromdrivespecifier"></a>Cdrom. drivespecifier

Die **drivespecifier** -Eigenschaft ruft den CD-oder DVD-Laufwerk Buchstaben ab.

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können. Diese Eigenschaft ruft einen laufwerkspezifizierer für einen NULL basierten Laufwerks Index innerhalb des mit *cdromcollection* abgerufenen Bereichs ab. **Anzahl**. Der abgerufene Wert hat die Form *x*:, wobei *X* den Laufwerk Buchstaben darstellt.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *CDROM* verwendet. **drivespecifier** zum Ausfüllen eines HTML-Text Bereichs namens MyText mit einer durch Trennzeichen getrennten Liste von verfügbaren CD-und DVD-Laufwerken. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player, Version 7,0 oder höher<br/>                               |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Cdromcollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





