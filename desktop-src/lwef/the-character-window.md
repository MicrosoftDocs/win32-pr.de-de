---
title: Das Zeichen Fenster
description: Das Zeichen Fenster
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391263"
---
# <a name="the-character-window"></a>Das Zeichen Fenster

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Microsoft-Agent zeigt animierte Zeichen in ihren eigenen Fenstern an, die immer am oberen Rand des Fensters z-Reihenfolge angezeigt werden (d. h. immer im Vordergrund). Ein Benutzer kann das Fenster eines Zeichens verschieben, indem er das Zeichen mit der linken Maustaste zieht. Das Zeichen Bild wird mit dem-Zeiger verschoben. Außerdem kann eine Anwendung mit der [**MoveTo**](moveto-method.md) -Methode ein Zeichen verschieben.

Wenn der Benutzer mit der rechten Maustaste auf ein Zeichen klickt, wird ein Popup Menü angezeigt, in dem die folgenden Befehle angezeigt werden:

\|Fenster schließen <span class="underline">V</span>Rach-Befehle Öffnen

<span class="underline">H</span>-IDE

----------------------------…

Get-Help\*


*Otherhostingapplicationcaption\*\**

\*Die aufgeführten Befehle basieren auf dem Eingabe aktiven Client. Weitere Informationen zum Definieren von Befehlen, die im Popup Menü angezeigt werden, finden Sie in der Übersicht über die Microsoft-Agent-Programmierschnittstelle.

\*\*Die aufgelisteten Einträge sind alle anderen Anwendungen, die zurzeit das Zeichen sind. Weitere Informationen zum Definieren dieses Eintrags finden Sie in der Übersicht über die Microsoft-Agent-Programmierschnittstelle.

Mit dem \| Fenster Befehl Schließen Stimmen Befehle öffnen wird die Anzeige des Befehls Fensters des aktuellen aktiven Zeichens gesteuert. Wenn sprach Erkennungs Dienste deaktiviert sind, ist dieser Befehl deaktiviert. Wenn sprach Erkennungs Dienste nicht installiert sind, wird dieser Befehl nicht angezeigt.

Der Hide-Befehl verbirgt das Zeichen. Die Animation, die dem **Versteck** Zustand des Zeichens zugewiesen ist, spielt das Zeichen und blendet es aus. Der Buchstabe "H" in Hide ist die Zugriffstaste des Befehls (mnetmonic).

Die Befehle für die Anwendung (en), die das Zeichen momentan als Host verwenden, folgen dem Hide-Befehl mit vorangestelltem Trennzeichen. Anschließend werden die Namen von anderen Anwendungen, die das Zeichen verwenden, mit einem Trennzeichen angezeigt.

 

 




