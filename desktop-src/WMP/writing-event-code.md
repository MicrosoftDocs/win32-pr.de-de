---
title: Schreiben von Ereignis Code
description: Schreiben von Ereignis Code
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player Skins, Schreiben von Code
- Skins, Schreiben von Code
- Ereignisse, Schreiben von Code
- Schreiben von Code für Skins, Informationen zu
- Windows Media Player Skins, Ereignisse
- Skins, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037569"
---
# <a name="writing-event-code"></a>Schreiben von Ereignis Code

Ereignisse werden ähnlich wie Attribute behandelt. Sie müssen dem Ereignis einen Wert übergeben, und der Wert ist der Code, den Sie ausführen möchten, wenn das Ereignis eintritt. Das Wort "on" wird am Anfang des Ereignis namens hinzugefügt. das Click-Ereignis wird z. b. auf **OnClick** fest.

Der Ereignis Wert ist in doppelten Anführungszeichen und beginnt mit dem Wort JScript gefolgt von einem Doppelpunkt. Der Code, den Sie ausführen möchten, wird als nächstes angezeigt, gefolgt von einem Semikolon und den schließenden doppelten Anführungszeichen. Wenn Sie z. b. die Wiedergabe beenden möchten, wenn der Benutzer auf eine Schaltfläche klickt, geben Sie Folgendes als Attribut in den Code des **Schalt** Flächen Elements ein:


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Wenn Sie über einen Code verfügen, der Anführungszeichen erfordert, verwenden Sie einfache Anführungszeichen. Es muss sorgfältig vorgegangen werden, wenn Anführungszeichen verwendet werden, damit Sie ordnungsgemäß ausgeglichen werden. Im folgenden finden Sie ein Beispiel für die Verwendung beider Typen:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



Sie können auch die Attribute Ihrer Skin ändern, wenn Sie ein externes Ereignis verarbeiten. Wenn Sie z. b. eine Ansicht mit dem Namen MyView schließen möchten, können Sie Folgendes eingeben:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




