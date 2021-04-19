---
title: Media. Duration
description: Die Duration-Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368690"
---
# <a name="mediaduration"></a>Media. Duration

Die **Duration** -Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **Dauer**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** ( **Double**).

## <a name="remarks"></a>Bemerkungen

, Wenn diese Eigenschaft mit einem anderen als dem in *Player* angegebenen Medien Element verwendet wird. **currentMedia** kann keinen gültigen Wert enthalten.

Zum Abrufen der Dauer für Dateien, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie auf das Öffnen der Datei durch Windows Media Player warten. Das heißt, dass der aktuelle openstate-Wert "mediaopen" entsprechen muss. Sie können dies überprüfen, indem Sie den *Player* verarbeiten. **OpenStateChange** -Ereignis oder durch regelmäßiges Überprüfen des Werts von *Player*. **openstate**.

Bei Wiedergabelisten kann die Dauer der einzelnen Medienelemente abgerufen werden, wenn das einzelne Medien Element geöffnet wird, anstatt beim Öffnen der Wiedergabeliste.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Im folgenden JScript-Beispiel werden *Medien* verwendet. **Dauer** , mit der die verbleibende Zeit im aktuellen Medien Element angezeigt wird. Ein HTML div-Element namens remtime zeigt die Informationen an. Ein HTML-Timer aktualisiert den Text im div-Element jede Sekunde.

Mit dem folgenden JScript-Code wird der Timer gestartet:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



Mit dem folgenden JScript-Code wird der Timer beendet:


```JScript
window.clearInterval(idTmr);
```



Verwenden Sie den *Player*. **PlayStateChange** -Ereignis mit einer **Switch** -Anweisung, um zu bestimmen, wann der Timer gestartet und angehalten werden soll.

Der folgende JScript-Code wird jedes Mal ausgeführt, wenn der Timer die Update-Funktion aufruft:


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. PlayStateChange-Ereignis**](player-player-playstatechange.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





