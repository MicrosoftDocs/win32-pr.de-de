---
title: Verwenden von Ereignissen mit asynchronen Aufrufen
description: Verwenden von Ereignissen mit asynchronen Aufrufen
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media-Format-SDK, Ereignisse mit asynchronen Aufrufen
- Windows Media-Format-SDK, asynchrone Ereignis Aufrufe
- Ereignisse, asynchrone Aufrufe
- asynchrone Aufrufe von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388635"
---
# <a name="using-events-with-asynchronous-calls"></a>Verwenden von Ereignissen mit asynchronen Aufrufen

Häufig können Sie bei der Verwendung von Methoden, die asynchron aufgerufen werden, die weitere Verarbeitung der Anwendung anhalten, bis die-Methode die Verarbeitung abgeschlossen hat. Sie können jedes Verfahren implementieren, das Sie für diese Situation ausführen möchten. In diesem Abschnitt wird beschrieben, wie Sie mit einem Ereignis auf asynchrone Aufrufe im aufrufenden Thread warten. Dieses Verfahren wird häufig mit dem SDK für den Windows Media-Format verwendet und wird in einigen der Beispielanwendungen veranschaulicht.

In der folgenden Liste wird die Verwendung von Ereignissen für das warten auf asynchrone Aufrufe zusammengefasst.

1.  Erstellen Sie ein Ereignis für die Verwendung mit Ihrer Anwendung, indem Sie die **CreateEvent** -Funktion des Platform SDK aufrufen.
2.  Wenn Sie die entsprechenden Rückrufe für die Anwendung implementieren, fangen Sie die Nachrichten ab, die Sie warten müssen. Signalisieren Sie in der Meldungs Behandlungs Logik für die gewünschten Nachrichten das Ereignis, indem Sie die Funktion " **settevent** " des Platform SDK aufrufen.
3.  Nachdem Aufrufe von asynchronen Ereignissen in der Anwendung vorgenommen wurden, warten Sie, bis das Ereignis signalisiert, indem Sie die **WaitForSingleObject** -Funktion des Platform SDK aufrufen. Wenn Sie eine Windows-Anwendung entwerfen, sollten Sie eine Schleife zum Überprüfen auf Windows-Meldungen erstellen und einen Aufruf von **WaitForSingleObject** in der Schleife mit einer kurzen Wartezeit einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden der Rückruf Methoden**](using-the-callback-methods.md)
</dt> </dl>

 

 




