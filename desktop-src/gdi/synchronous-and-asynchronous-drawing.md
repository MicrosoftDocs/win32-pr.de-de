---
description: Die meisten Zeichen, die während der Verarbeitung der WM PAINT-Nachricht ausgeführt werden, sind asynchron. Das heißt, es gibt eine Verzögerung zwischen dem Zeitpunkt, zu dem ein Teil des Fensters ungültig wird, und der Zeit, zu der \_ WM \_ PAINT gesendet wird.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Synchrones und asynchrones Zeichnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e22b49a61d021c886da6253a2575c0e7f1c7a8c01eb2c3b550e04acda5daf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613390"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Synchrones und asynchrones Zeichnen

Die meisten Zeichen, die während der Verarbeitung der [**WM \_ PAINT-Nachricht**](wm-paint.md) ausgeführt werden, sind asynchron. Das heißt, es gibt eine Verzögerung zwischen dem Zeitpunkt, zu dem ein Teil des Fensters ungültig wird, und der Zeit, zu der WM \_ PAINT gesendet wird. Während der Verzögerung ruft die Anwendung in der Regel Nachrichten aus der Warteschlange ab und führt andere Aufgaben aus. Der Grund für die Verzögerung ist, dass das System das Zeichnen in einem Fenster im Allgemeinen als Vorgang mit niedriger Priorität behandelt und so funktioniert, als ob Benutzereingabenachrichten und Meldungen, die sich auf die Position oder Größe eines Fensters auswirken können, vor WM PAINT verarbeitet \_ werden.

In einigen Fällen ist es erforderlich, dass eine Anwendung synchron zeichnen kann, d. &a. im Fenster unmittelbar nach dem Ungültig machen eines Teils des Fensters. Eine typische Anwendung zeichnet ihr Hauptfenster unmittelbar nach dem Erstellen des Fensters, um dem Benutzer zu signalisieren, dass die Anwendung erfolgreich gestartet wurde. Das System zeichnet einige Steuerfenster synchron, z. B. Schaltflächen, da solche Fenster als Fokus für Benutzereingaben dienen. Obwohl jedes Fenster mit einer einfachen Zeichnungsroutine synchron gezeichnet werden kann, sollten alle diese Zeichnungen schnell durchgeführt werden und die Fähigkeit der Anwendung, auf Benutzereingaben zu reagieren, nicht beeinträchtigen.

Die [**Funktionen UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) [**und RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) ermöglichen synchrones Zeichnen. **UpdateWindow sendet** eine [**WM \_ PAINT-Nachricht**](wm-paint.md) direkt an das Fenster, wenn der Updatebereich nicht leer ist. **RedrawWindow** sendet auch eine **WM \_ PAINT-Nachricht,** gibt der Anwendung jedoch mehr Kontrolle darüber, wie das Fenster gezeichnet werden soll, z. B. ob der Nichtclientbereich und der Fensterhintergrund gezeichnet werden oder ob die Nachricht gesendet werden soll, unabhängig davon, ob der Updatebereich leer ist. Diese Funktionen senden die **WM \_ PAINT-Nachricht** direkt an das Fenster, unabhängig von der Anzahl der anderen Nachrichten in der Anwendungsnachrichtenwarteschlange.

Jedes Fenster, das zeitaufwändige Zeichnungsvorgänge erfordert, sollte asynchron gezeichnet werden, um zu verhindern, dass ausstehende Meldungen beim Zeichnen des Fensters blockiert werden. Außerdem sollte jede Anwendung, die häufig kleine Teile eines Fensters für ungültig erklärt, zulassen, dass diese ungültigen Teile in einer einzigen asynchronen [**WM \_ PAINT-Nachricht**](wm-paint.md) konsolidiert werden, anstatt in einer Reihe synchroner **WM \_ PAINT-Nachrichten.**

 

 



