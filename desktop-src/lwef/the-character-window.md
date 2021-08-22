---
title: Das Zeichenfenster
description: Das Zeichenfenster
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426aab4cbd6e0ad536135cb47ec9a636ea56a0509f3fb0cb75ad6440addc62da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474886"
---
# <a name="the-character-window"></a>Das Zeichenfenster

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Der Microsoft-Agent zeigt animierte Zeichen in ihren eigenen Fenstern an, die immer oben im Fenster Z-Reihenfolge angezeigt werden (d.amp;#160;D. B. immer oben). Ein Benutzer kann das Fenster eines Zeichens verschieben, indem er das Zeichen mit der linken Maustaste zieht. Das Zeichenbild wird mit dem Zeiger verschoben. Darüber hinaus kann eine Anwendung ein Zeichen mithilfe der [**MoveTo-Methode**](moveto-method.md) verschieben.

Wenn der Benutzer mit der rechten Maustaste auf ein Zeichen klickt, wird ein Popupmenü mit den folgenden Befehlen angezeigt:

Öffnen \| Des Fensters <span class="underline">"Vice-Befehle</span>schließen"

<span class="underline">H-ide</span>

----------------------------…

Befehl\*


*OtherHostingApplicationCaption\*\**

\*Die aufgeführten Befehle basieren auf dem eingabeaktiven Client. Weitere Informationen zum Definieren von Befehlen, die im Popupmenü angezeigt werden, finden Sie unter Übersicht über die Microsoft-Agent-Programmierschnittstelle.

\*\*Die aufgeführten Einträge sind alle anderen Anwendungen, die das Zeichen derzeit hosten. Weitere Informationen zum Definieren dieses Eintrags finden Sie unter Übersicht über die Programmierschnittstelle für Microsoft-Agents.

Der Befehl Open \| Close Voice Commands Window steuert die Anzeige des Befehlsfensters des aktuellen aktiven Zeichens. Wenn Spracherkennungsdienste deaktiviert sind, ist dieser Befehl deaktiviert. Wenn spracherkennungsdienste nicht installiert sind, wird dieser Befehl nicht angezeigt.

Der Befehl Ausblenden blendet das Zeichen aus. Die Animation, die dem **Ausblenden-Zustand** des Zeichens zugewiesen ist, wird wiedergegeben und blendet das Zeichen aus. Der im Ausblenden enthaltene Buchstabe "H" ist der Zugriffsschlüssel des Befehls (mnemonic).

Die Befehle für die Anwendungen, die das Zeichen derzeit hosten, folgen dem Befehl Ausblenden, dem ein Trennzeichen vorangestellt ist. Anschließend werden die Namen anderer Anwendungen, die das Zeichen verwenden, angezeigt, dem auch ein Trennzeichen vorangestellt ist.

 

 




