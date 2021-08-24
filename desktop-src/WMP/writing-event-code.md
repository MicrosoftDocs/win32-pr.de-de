---
title: Schreiben von Ereigniscode
description: Schreiben von Ereigniscode
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player Skins, Schreiben von Code
- Skins,Schreiben von Code
- Ereignisse,Schreiben von Code
- Schreiben von Code für Skins, Informationen
- Windows Media Player Skins, Ereignisse
- Skins, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39c35864151db1671c2f7fa94caea803f0a33cc1082a3ae44082a90f7bddafb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760570"
---
# <a name="writing-event-code"></a>Schreiben von Ereigniscode

Ereignisse werden ähnlich wie Attribute behandelt. Sie müssen dem Ereignis einen Wert geben, und der Wert ist der Code, den Sie ausführen möchten, wenn das Ereignis eintritt. Das Wort "on" wird am Ende des Ereignisnamens hinzugefügt. Beispielsweise wird das Klickereignis zu **onclick**.

Der Ereigniswert ist in doppelten Anführungszeichen angegeben und beginnt mit dem Wort JScript gefolgt von einem Doppelpunkt. Als Nächstes folgt der Code, den Sie ausführen möchten, gefolgt von einem Semikolon und den schließenden doppelten Anführungszeichen. Um beispielsweise die Wiedergabe zu beenden, wenn der Benutzer auf eine Schaltfläche klickt, geben Sie Folgendes als Attribut in Ihren **BUTTON-Elementcode** ein:


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Wenn Sie über einen Code verfügen, der Anführungszeichen erfordert, verwenden Sie einfache Anführungszeichen. Wenn Sie Anführungszeichen verwenden, müssen Sie darauf achten, dass sie ordnungsgemäß ausgeglichen sind. Im Folgenden finden Sie ein Beispiel für die Verwendung beider Typen:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



Sie können die Attribute Ihrer Skin auch ändern, wenn Sie ein externes Ereignis behandeln. Um z. B. eine Ansicht mit dem Namen myView zu schließen, können Sie Folgendes eingeben:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Ereignissen**](handling-events.md)
</dt> </dl>

 

 




