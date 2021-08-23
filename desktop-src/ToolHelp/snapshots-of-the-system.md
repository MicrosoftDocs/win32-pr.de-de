---
title: Momentaufnahmen des Systems
description: Momentaufnahmen sind der Kern der Toolhilfefunktionen. Eine Momentaufnahme ist eine schreibgeschützte Kopie des aktuellen Zustands einer oder mehreren der folgenden Listen, die sich in Systemspeicherprozessen, Threads, Modulen und Heaps befinden.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30dde3a4383bf56bdef46c59c55611ffe9b22a7a201abb4f0f11af85594c4f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137413"
---
# <a name="snapshots-of-the-system"></a>Momentaufnahmen des Systems

Momentaufnahmen sind der Kern der Toolhilfefunktionen. Eine Momentaufnahme ist eine schreibgeschützte Kopie des aktuellen Zustands einer oder mehreren der folgenden Listen, die sich im Systemspeicher befinden: Prozesse, Threads, Module und Heaps.

Prozesse, die Toolhilfefunktionen verwenden, greifen auf diese Listen von Momentaufnahmen statt direkt vom Betriebssystem aus zu. Die Listen im Systemspeicher ändern sich, wenn Prozesse gestartet und beendet werden, Threads erstellt und zerstört werden, ausführbare Module geladen und aus dem Systemspeicher entladen und Heaps erstellt und zerstört werden. Die Verwendung von Informationen aus einer Momentaufnahme verhindert Inkonsistenzen. Andernfalls können Änderungen an einer Liste möglicherweise dazu führen, dass ein Thread die Liste falsch durchläuft oder eine Zugriffsverletzung (einen GP-Fehler) verursacht. Wenn beispielsweise eine Anwendung die Threadliste durchläuft, während andere Threads erstellt oder beendet werden, werden informationen, die die Anwendung zum Durchlaufen der Threadliste verwendet, möglicherweise veraltet und können einen Fehler für die Anwendung verursachen, die die Liste durchläuft.

Verwenden Sie die Funktion [**CreateToolhelp32Snapshot,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) um eine Momentaufnahme des Systemspeichers zu erstellen. Sie können den Inhalt einer Momentaufnahme steuern, indem Sie beim Aufrufen dieser Funktion einen oder mehrere der folgenden Werte angeben:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Die **Werte für TH32CS \_ SNAPHEAPLIST** und **TH32CS \_ SNAPMODULE** sind prozessspezifisch. Wenn diese Werte angegeben werden, werden die Heap- und Modullisten des angegebenen Prozesses in die Momentaufnahme aufgenommen. Wenn Sie null als Prozessbezeichner angeben, wird der aktuelle Prozess verwendet. Der **TH32CS \_ SNAPTHREAD-Wert** erstellt immer eine systemweite Momentaufnahme, auch wenn ein Prozessbezeichner an [**CreateToolhelp32Snapshot übergeben wird.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)

Um den Heap- oder Modulzustand für alle Prozesse aufzählen zu können, geben Sie den **TH32CS \_ SNAPALL-Wert** und den Prozessbezeichner des aktuellen Prozesses an. Rufen Sie dann für jeden zusätzlichen Prozess in der Momentaufnahme [**erneut CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) auf, und geben Sie dabei den Prozessbezeichner und den **TH32CS \_ SNAPHEAPLIST-** oder **TH32CS \_ SNAPMODULE-Wert** an.

Sie können einen erweiterten Fehlerstatuscode für [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) mithilfe der [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) abrufen.

Wenn der Prozess die Verwendung einer Momentaufnahme abgeschlossen hat, zerstören Sie sie mithilfe der [**CloseHandle-Funktion.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Wenn Sie eine Momentaufnahme nicht zerstören, gibt der Prozess Arbeitsspeicher ab, bis er beendet wird. Zu diesem Zeitpunkt gibt das System den Arbeitsspeicher zurück.

> [!Note]  
> Das Momentaufnahmehand handle verhält sich wie ein Dateihand handle und unterliegt den gleichen Regeln in Bezug auf die Prozesse und Threads, in denen es verwendet werden kann. Um anzugeben, dass das Handle vererbbar ist, erstellen Sie die Momentaufnahme mithilfe des **TH32CS \_ INHERIT-Werts.**

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Momentaufnahme und Anzeigen von Prozessen](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 