---
title: Media.duration
description: Die duration-Eigenschaft ruft die Dauer des aktuellen Medienelements in Sekunden ab.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media.duration Windows Media Player
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
ms.openlocfilehash: e89eab1ffbb8c9f3d48c3f61eb6d831af66b4931ed1d858658eed3fc21d08183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118800"
---
# <a name="mediaduration"></a>Media.duration

Die **duration-Eigenschaft** ruft die Dauer des aktuellen Medienelements in Sekunden ab.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **duration**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** ( **double**).

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft mit einem anderen Medienelement als dem in *Player* angegebenen verwendet wird. **currentMedia**, es darf keinen gültigen Wert enthalten.

Um die Dauer für Dateien abzurufen, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie warten, bis Windows Media Player die Datei öffnet. Das bedeutet, dass der aktuelle OpenState gleich MediaOpen sein muss. Sie können dies überprüfen, indem Sie den *Player* behandeln. **OpenStateChange-Ereignis** oder durch regelmäßiges Überprüfen des Werts von *Player*. **openState**.

Bei Wiedergabelisten kann die Dauer jedes Medienelements abgerufen werden, wenn das einzelne Medienelement geöffnet wird, und nicht die , wenn die Wiedergabeliste geöffnet wird.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Im folgenden JScript Beispiel wird *Media verwendet.* **dauer,** um die verbleibende Zeit im aktuellen Medienelement anzuzeigen. Ein HTML-DIV-Element mit dem Namen RemTime zeigt die Informationen an. Ein HTML-Timer aktualisiert den Text im DIV-Element jede Sekunde.

Mit dem folgenden JScript Code wird der Timer gestartet:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



Mit dem folgenden JScript Code wird der Timer beendet:


```JScript
window.clearInterval(idTmr);
```



Verwenden Sie den *Player*. **PlayStateChange-Ereignis** mit einer **switch-Anweisung,** um zu bestimmen, wann der Timer gestartet und beendet werden soll.

Der folgende JScript Code wird jedes Mal ausgeführt, wenn der Timer die Updatefunktion aufruft:


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.PlayStateChange-Ereignis**](player-player-playstatechange.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





