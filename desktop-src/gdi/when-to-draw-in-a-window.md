---
description: 'Eine Anwendung wird in einem Fenster zu verschiedenen Zeitpunkten gezeichnet: bei der ersten Erstellung eines Fensters, beim Ändern der Fenstergröße, beim Ändern des Fensters von einem anderen Fenster, beim minimieren oder maximieren des Fensters, beim Anzeigen von Daten aus einer geöffneten Datei und beim Scrollen, ändern oder Auswählen eines Teils der angezeigten Daten.'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Wann in einem Fenster gezeichnet werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345138"
---
# <a name="when-to-draw-in-a-window"></a>Wann in einem Fenster gezeichnet werden soll

Eine Anwendung wird in einem Fenster zu verschiedenen Zeitpunkten gezeichnet: bei der ersten Erstellung eines Fensters, beim Ändern der Fenstergröße, beim Ändern des Fensters von einem anderen Fenster, beim minimieren oder maximieren des Fensters, beim Anzeigen von Daten aus einer geöffneten Datei und beim Scrollen, ändern oder Auswählen eines Teils der angezeigten Daten.

Das System verwaltet Aktionen wie das Verschieben und die Größenanpassung eines Fensters. Wenn sich eine Aktion auf den Inhalt des Fensters auswirkt, markiert das System den betroffenen Teil des Fensters als bereit für die Aktualisierung und sendet bei der nächsten Gelegenheit eine [**WM \_ Paint**](wm-paint.md) -Meldung an die Fenster Prozedur des Fensters. Die Meldung ist ein Signal an die Anwendung, um zu bestimmen, was aktualisiert werden muss, und um die erforderliche Zeichnung auszuführen.

Einige Aktionen werden von der Anwendung verwaltet, z. b. das Anzeigen von geöffneten Dateien und das Auswählen von angezeigten Daten. Für diese Aktionen kann eine Anwendung markieren, um den Teil des Fensters zu aktualisieren, der von der Aktion betroffen ist, was dazu führt, dass bei der nächsten Gelegenheit eine [**WM- \_ Paint**](wm-paint.md) -Meldung gesendet wird. Wenn eine Aktion sofortiges Feedback erfordert, kann die Anwendung zeichnen, während die Aktion stattfindet, ohne auf die **WM- \_ Farbe** zu warten. Beispielsweise hebt eine typische Anwendung den Bereich hervor, den der Benutzer auswählt, anstatt darauf zu warten, dass die nächste WM-Zeichnungs Meldung den Bereich aktualisiert. **\_**

In allen Fällen kann eine Anwendung in einem Fenster gezeichnet werden, sobald Sie erstellt wird. Um im Fenster zu zeichnen, muss die Anwendung zunächst ein Handle für einen Anzeigegeräte Kontext für das Fenster abrufen. Im Idealfall führt eine Anwendung die meisten Zeichnungsvorgänge während der Verarbeitung von WM- [**Zeichnungs \_**](wm-paint.md) Nachrichten aus. In diesem Fall ruft die Anwendung einen Anzeigegeräte Kontext durch Aufrufen der [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion ab. Wenn eine Anwendung zu einem beliebigen Zeitpunkt erstellt wird, z. b. in [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) oder während der Verarbeitung von Tastatur-oder Maus Nachrichten, ruft Sie die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion oder die [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion auf, um den Anzeige-DC abzurufen.

 

 
