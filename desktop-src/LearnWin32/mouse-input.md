---
title: Mauseingabe (Erste Schritte mit Win32 und C++)
description: Mauseingabe
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ff39b798b1438bca33bc9ab9b077333dca351e32a5945b939beba2c13f5894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897044"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Mauseingabe (Erste Schritte mit Win32 und C++)

Windows unterstützt Mausen mit bis zu fünf Schaltflächen: links, mitte und rechts sowie zwei zusätzliche Schaltflächen namens XBUTTON1 und XBUTTON2.

![Abbildung, die die Schaltflächen links (1), rechts (2), mittel (3) und xbutton1 (4) zeigt.](images/mouse.png)

Die meisten Mauschen für Windows verfügen mindestens über die schaltflächen links und rechts. Die linke Maustaste wird zum Zeigen, Auswählen, Ziehen usw. verwendet. Mit der rechten Maustaste wird in der Regel ein Kontextmenü angezeigt. Einige Mausen verfügen über ein Scrollrad zwischen den schaltflächen links und rechts. Je nach Maus ist das Scrollrad möglicherweise auch klickbar, sodass es die mittlere Schaltfläche ist.

Die Schaltflächen XBUTTON1 und XBUTTON2 befinden sich häufig an den Seiten der Maus in der Nähe der Basis. Diese zusätzlichen Schaltflächen sind nicht auf allen Mausen vorhanden. Falls vorhanden, werden die Schaltflächen XBUTTON1 und XBUTTON2 häufig einer Anwendungsfunktion zugeordnet, z. B. der Vorwärts- und Rückwärtsnavigation in einem Webbrowser.

Linkshändige Benutzer finden es häufig bequemer, die Funktionen der linken und rechten Schaltflächen auszutauschen– indem sie die rechte Schaltfläche als Zeiger und die linke Schaltfläche verwenden, um das Kontextmenü anzuzeigen. Aus diesem Grund werden in der Windows Hilfedokumentation die Begriffe *primäre Schaltfläche* und *sekundäre Schaltfläche* verwendet, die sich auf die logische Funktion und nicht auf die physische Platzierung beziehen. In der Standardeinstellung (rechtshändig) ist die linke Schaltfläche die primäre Schaltfläche und die rechte die sekundäre Schaltfläche. Die Begriffe *rechtsklick* und *linker Klick* beziehen sich jedoch auf logische Aktionen. *Rechtsklick* bedeutet, auf die primäre Schaltfläche zu klicken, unabhängig davon, ob sich diese Schaltfläche physisch auf der rechten oder linken Seite der Maus befindet.

Unabhängig davon, wie der Benutzer die Maus konfiguriert, übersetzt Windows Automatisch Mausnachrichten, damit sie konsistent sind. Der Benutzer kann die primären und sekundären Schaltflächen während der Verwendung des Programms tauschen und wirkt sich nicht auf das Verhalten Des Programms aus.

In der MSDN-Dokumentation werden die Begriffe *"Schaltfläche rechts"* und *"Linke Schaltfläche"* als *primäre* und *sekundäre* Schaltfläche verwendet. Diese Terminologie stimmt mit den Namen der Fenstermeldungen für Mauseingaben überein. Denken Sie daran, dass die physischen linken und rechten Schaltflächen möglicherweise ausgetauscht werden.

## <a name="next"></a>Nächste

[Reagieren auf Mausklicks](mouse-clicks.md)

 

 




