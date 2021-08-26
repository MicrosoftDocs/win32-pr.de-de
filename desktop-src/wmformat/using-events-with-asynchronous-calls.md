---
title: Verwenden von Ereignissen mit asynchronen Aufrufen
description: Verwenden von Ereignissen mit asynchronen Aufrufen
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK,Ereignisse mit asynchronen Aufrufen
- Windows Medienformat-SDK, asynchrone Aufrufereignisse
- Ereignisse,asynchrone Aufrufe
- asynchrone Aufrufereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd315b56570419afd81aa3300cfa3ee1dd907e22310aba79432e4533f99a82db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929130"
---
# <a name="using-events-with-asynchronous-calls"></a>Verwenden von Ereignissen mit asynchronen Aufrufen

Wenn Sie Methoden verwenden, die asynchron aufgerufen werden, sollten Sie häufig die weitere Verarbeitung Ihrer Anwendung anhalten, bis die Verarbeitung der Methode abgeschlossen ist. Sie können eine beliebige Technik implementieren, um diese Situation zu behandeln. In diesem Abschnitt wird die Verwendung eines Ereignisses zum Warten auf asynchrone Aufrufe im aufrufenden Thread beschrieben. Diese Technik wird häufig mit dem Windows Media Format SDK verwendet und wird in einigen Beispielanwendungen demonstriert.

Die folgende Liste fasst die Verwendung von Ereignissen zum Warten auf asynchrone Aufrufe zusammen.

1.  Erstellen Sie ein Ereignis für die Verwendung mit Ihrer Anwendung, indem Sie die **CreateEvent-Funktion** des Platform SDK aufrufen.
2.  Wenn Sie die entsprechenden Rückrufe für Ihre Anwendung implementieren, fangen Sie die Nachrichten ab, auf die Sie warten müssen. Signalisieren Sie in der Nachrichtenverarbeitungslogik für die gewünschten Nachrichten das Ereignis, indem Sie die **SetEvent-Funktion** des Platform SDK aufrufen.
3.  Nachdem Aufrufe asynchroner Ereignisse in Ihrer Anwendung erfolgt sind, warten Sie, bis das Ereignis signalisiert wird, indem Sie die **WaitForSingleObject-Funktion** des Platform SDK aufrufen. Wenn Sie eine Windows-Anwendung entwerfen, sollten Sie eine Schleife erstellen, um nach Windows-Nachrichten zu suchen und einen Aufruf von **WaitForSingleObject** in die Schleife mit einer kurzen Wartezeit einschlussen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückrufmethoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




