---
title: Maus Eingaben (beginnen Sie mit Win32 und C++)
description: Mauseingabe
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339107"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Maus Eingaben (beginnen Sie mit Win32 und C++)

Windows unterstützt Mäuse mit bis zu fünf Schaltflächen: Links, zentriert und rechts sowie zwei zusätzliche Schaltflächen namens XButton1 und XButton2.

![eine Abbildung, in der die Schaltflächen links (1), rechts (2), Mittel (3) und XButton1 (4) angezeigt werden.](images/mouse.png)

Die meisten Mäuse für Windows haben mindestens die linke und die Rechte Schaltfläche. Die linke Maustaste wird zum zeigen, auswählen, ziehen usw. verwendet. Mit der rechten Maustaste wird in der Regel ein Kontextmenü angezeigt. Einige Mäuse haben ein Mausrad zwischen den linken und rechten Schaltflächen. Abhängig von der Maus kann das Mausrad auch klickbar sein, sodass es die mittlere Schaltfläche ist.

Die Schaltflächen XButton1 und XButton2 befinden sich häufig auf den Seiten der Maus, in der Nähe der Basis. Diese zusätzlichen Schaltflächen sind nicht auf allen Mäusen vorhanden. Falls vorhanden, werden die Schaltflächen XButton1 und XButton2 häufig einer Anwendungsfunktion zugeordnet, z. b. vorwärts-und rückwärts Navigation in einem Webbrowser.

Links übergebene Benutzer finden es häufig besser, die Funktionen der linken und rechten Schaltflächen auszutauschen – indem Sie die Rechte Schaltfläche als Zeiger und die linke Schaltfläche verwenden, um das Kontextmenü anzuzeigen. Aus diesem Grund werden in der Windows-Hilfe Dokumentation die Begriffe *primär Schaltfläche* und *Sekundär Schaltfläche* verwendet, die auf die logische Funktion und nicht auf die physische Platzierung verweisen. In der Standardeinstellung (rechtsseitig übergeben) ist die linke Schaltfläche die primäre Schaltfläche, und die Rechte Taste ist die sekundäre Schaltfläche. Die Begriffe mit der *rechten Maustaste klicken* und mit der *linken Maustaste* auf logische Aktionen verweisen. Klicken Sie mit der *rechten Maustaste* auf die Schaltfläche primär, und zwar unabhängig davon, ob sich die Schaltfläche auf der rechten oder linken Seite der Maus befindet.

Unabhängig davon, wie der Benutzer die Maus konfiguriert, übersetzt Windows automatisch Maus Meldungen, sodass Sie konsistent sind. Der Benutzer kann die primären und sekundären Schaltflächen in der Mitte der Verwendung des Programms austauschen und wirkt sich nicht darauf aus, wie sich das Programm verhält.

Die MSDN-Dokumentation verwendet die Schaltfläche mit den *rechten* und die *linke Schalt* Fläche, um die Schaltfläche *primär* und *Sekundär* Diese Terminologie ist mit den Namen der Fenster Meldungen für Maus Eingaben konsistent. Beachten Sie, dass die physischen linken und rechten Schaltflächen möglicherweise ausgetauscht werden.

## <a name="next"></a>Nächste

[Antworten auf Mausklicks](mouse-clicks.md)

 

 




