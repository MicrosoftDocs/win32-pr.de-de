---
description: Die meisten Zeichnungen, die während der Verarbeitung der WM-Zeichnungs Nachricht durchgeführt werden, \_ sind asynchron. das heißt, es gibt eine Verzögerung zwischen dem Zeitpunkt, zu dem ein Teil des Fensters ungültig wird, und der Zeit, zu der WM gezeichnet wird \_ .
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Synchrone und asynchrone Zeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960592"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Synchrone und asynchrone Zeichnung

Die meisten Zeichnungen, die während der Verarbeitung [**der \_ WM**](wm-paint.md) -Zeichnungs Nachricht durchgeführt werden, sind asynchron. das heißt, es gibt eine Verzögerung zwischen dem Zeitpunkt, zu dem ein Teil des Fensters ungültig wird, und der Zeit, zu der WM gezeichnet wird \_ . Während der Verzögerung Ruft die Anwendung normalerweise Nachrichten aus der Warteschlange ab und führt andere Aufgaben aus. Der Grund für die Verzögerung ist, dass das System in der Regel das Zeichnen in einem Fenster als Vorgang mit niedriger Priorität behandelt und so funktioniert, als ob Benutzereingaben und Meldungen, die sich auf die Position oder Größe eines Fensters auswirken können, vor WM Paint verarbeitet werden \_ .

In einigen Fällen ist es erforderlich, dass eine Anwendung synchron gezeichnet wird, indem Sie im Fenster sofort nach dem Aufheben eines Teils des Fensters zeichnen. Eine typische Anwendung zeichnet das Hauptfenster sofort nach dem Erstellen des Fensters, um dem Benutzer zu signalisieren, dass die Anwendung erfolgreich gestartet wurde. Das System zeichnet einige Steuerelement Fenster synchron, z. b. Schaltflächen, da solche Fenster als Fokus für Benutzereingaben dienen. Obwohl jedes Fenster mit einer einfachen Zeichnungs Routine synchron gezeichnet werden kann, sollten alle diese Zeichen schnell ausgeführt werden und sollten nicht die Fähigkeit der Anwendung beeinträchtigen, auf Benutzereingaben zu reagieren.

Die Funktionen [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) und [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) ermöglichen das synchrone zeichnen. **UpdateWindow** sendet eine [**WM \_**](wm-paint.md) -Zeichnungs Nachricht direkt an das Fenster, wenn der Aktualisierungs Bereich nicht leer ist. **Redrawwindow** sendet außerdem eine **WM \_** -Zeichnungs Nachricht, bietet der Anwendung jedoch eine bessere Kontrolle darüber, wie das Fenster gezeichnet werden soll, z. b. ob der nicht-Client Bereich und der Fenster Hintergrund gezeichnet werden sollen oder ob die Nachricht unabhängig davon, ob der Aktualisierungs Bereich leer ist, gesendet werden soll. Diese Funktionen senden die **WM \_** -Zeichnungs Nachricht unabhängig von der Anzahl anderer Nachrichten in der Nachrichten Warteschlange der Anwendung direkt an das-Fenster.

Jedes Fenster, das zeitaufwändige Zeichnungsvorgänge erfordert, muss asynchron gezeichnet werden, um zu verhindern, dass ausstehende Nachrichten blockiert werden, wenn das Fenster gezeichnet wird. Außerdem sollten alle Anwendungen, die kleine Teile eines Fensters häufig für ungültig erklären, zulassen, dass diese ungültigen Teile in einer einzigen asynchronen WM-Zeichnungs Nachricht und nicht in einer Reihe synchroner **WM \_** -Zeichnungs Nachrichten konsolidiert werden. [**\_**](wm-paint.md)

 

 



