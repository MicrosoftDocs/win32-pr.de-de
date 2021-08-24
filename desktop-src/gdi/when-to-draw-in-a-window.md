---
description: 'Eine Anwendung zeichnet in einem Fenster zu verschiedenen Zeiten: beim ersten Erstellen eines Fensters, beim Ändern der Fenstergröße, beim Verschieben des Fensters hinter ein anderes Fenster, beim Minimieren oder Maximieren des Fensters, beim Anzeigen von Daten aus einer geöffneten Datei und beim Scrollen, Ändern oder Auswählen eines Teils der angezeigten Daten.'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Wann in einem Fenster ge zeichnen werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832f219ad15fa919715b0f6892b73686237e1c3681e298106db3cefc4a8c3ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468090"
---
# <a name="when-to-draw-in-a-window"></a>Wann in einem Fenster ge zeichnen werden soll

Eine Anwendung zeichnet in einem Fenster zu verschiedenen Zeiten: beim ersten Erstellen eines Fensters, beim Ändern der Fenstergröße, beim Verschieben des Fensters hinter ein anderes Fenster, beim Minimieren oder Maximieren des Fensters, beim Anzeigen von Daten aus einer geöffneten Datei und beim Scrollen, Ändern oder Auswählen eines Teils der angezeigten Daten.

Das System verwaltet Aktionen wie das Verschieben und Anpassen der Größe eines Fensters. Wenn eine Aktion den Inhalt des Fensters beeinflusst, markiert das System den betroffenen Teil des Fensters als bereit für die Aktualisierung und sendet bei der nächsten Gelegenheit eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an die Fensterprozedur des Fensters. Die Nachricht ist ein Signal an die Anwendung, um zu bestimmen, was aktualisiert werden muss, und um die erforderliche Zeichnung durchführen zu können.

Einige Aktionen werden von der Anwendung verwaltet, z. B. das Anzeigen geöffneter Dateien und das Auswählen der angezeigten Daten. Für diese Aktionen kann eine Anwendung für die Aktualisierung des Teils des Fensters markieren, der von der Aktion betroffen ist, was dazu führt, dass bei der nächsten Gelegenheit eine [**WM \_ PAINT-Nachricht**](wm-paint.md) gesendet wird. Wenn eine Aktion sofortiges Feedback erfordert, kann die Anwendung zeichnen, während die Aktion stattfindet, ohne auf **WM \_ PAINT zu warten.** Beispielsweise hebt eine typische Anwendung den Bereich hervor, den der Benutzer auswählt, anstatt darauf zu warten, dass die nächste **WM \_ PAINT-Nachricht** den Bereich aktualisiert.

In jedem Fall kann eine Anwendung in einem Fenster zeichnen, sobald sie erstellt wird. Um im Fenster zu zeichnen, muss die Anwendung zunächst ein Handle für einen Anzeigegerätekontext für das Fenster abrufen. Im Idealfall führt eine Anwendung die meisten Zeichenvorgänge während der Verarbeitung von [**WM \_ PAINT-Nachrichten**](wm-paint.md) aus. In diesem Fall ruft die Anwendung einen Anzeigegerätekontext ab, indem die [**BeginPaint-Funktion aufgerufen**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) wird. Wenn eine Anwendung zu einem anderen Zeitpunkt zeichnet, z. B. aus [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) oder während der Verarbeitung von Tastatur- oder Mausnachrichten, ruft sie die [**GetDC-**](/windows/desktop/api/Winuser/nf-winuser-getdc) oder [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) auf, um den Anzeige-DC abzurufen.

 

 
