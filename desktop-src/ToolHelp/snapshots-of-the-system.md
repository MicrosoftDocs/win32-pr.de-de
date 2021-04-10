---
title: Momentaufnahmen des Systems
description: Momentaufnahmen sind das Kernstück der Tool Hilfefunktionen. Eine Momentaufnahme ist eine schreibgeschützte Kopie des aktuellen Status einer oder mehrerer der folgenden Listen, die sich in Systemspeicher Prozessen, Threads, Modulen und Heaps befinden.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858350"
---
# <a name="snapshots-of-the-system"></a>Momentaufnahmen des Systems

Momentaufnahmen sind das Kernstück der Tool Hilfefunktionen. Eine Momentaufnahme ist eine schreibgeschützte Kopie des aktuellen Status einer oder mehrerer der folgenden Listen, die sich im Systemspeicher befinden: Prozesse, Threads, Module und Heaps.

Prozesse, die Tool Hilfefunktionen verwenden, greifen auf diese Listen von Momentaufnahmen anstatt direkt vom Betriebssystem aus zu. Die Listen im Systemspeicher ändern sich, wenn Prozesse gestartet und beendet werden, Threads erstellt und zerstört werden, ausführbare Module geladen und aus dem Systemspeicher entladen werden und Heaps erstellt und zerstört werden. Die Verwendung von Informationen aus einer Momentaufnahme verhindert Inkonsistenzen. Andernfalls können Änderungen an einer Liste möglicherweise bewirken, dass ein Thread die Liste fälschlicherweise durchläuft oder eine Zugriffsverletzung verursacht (ein GP-Fehler). Wenn eine Anwendung z. b. die Thread Liste durchläuft, während andere Threads erstellt oder beendet werden, kann es vorkommen, dass die von der Anwendung zum Durchlaufen der Thread Liste verwendeten Informationen veraltet sind und einen Fehler für die Anwendung verursachen können, die die Liste durchläuft.

Verwenden Sie die [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) -Funktion, um eine Momentaufnahme des System Speichers zu erstellen. Wenn Sie diese Funktion aufrufen, können Sie den Inhalt einer Momentaufnahme steuern, indem Sie einen oder mehrere der folgenden Werte angeben:

-   **TH32CS \_ snapheaplist**
-   **TH32CS \_ snapmodule**
-   **TH32CS \_ snapprocess**
-   **TH32CS \_ snapthreadthread**

Die **TH32CS \_ snapheaplist** -und **TH32CS \_ snapmodule** -Werte sind Prozess spezifisch. Wenn diese Werte angegeben werden, sind die Heap-und Modul Listen des angegebenen Prozesses in der Momentaufnahme enthalten. Wenn Sie NULL als Prozess-ID angeben, wird der aktuelle Prozess verwendet. Der **TH32CS \_ snapthread** -Wert erstellt immer eine systemweite Momentaufnahme, auch wenn eine Prozess-ID an [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)weitergegeben wird.

Um den Heap-oder Modul Zustand für alle Prozesse aufzulisten, geben Sie den **TH32CS \_ snapall** -Wert und den Prozess Bezeichner des aktuellen Prozesses an. Anschließend wird für jeden zusätzlichen Prozess in der Momentaufnahme [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) erneut aufgerufen. dabei werden die Prozess-ID und der **TH32CS \_ snapheaplist** -oder **TH32CS \_ snapmodule** -Wert angegeben.

Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) abrufen.

Wenn der Prozess mit einer Momentaufnahme abgeschlossen ist, zerstören Sie ihn mithilfe der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion. Wenn Sie eine Momentaufnahme nicht zerstören, wird der Arbeitsspeicher vom Prozess bis zum Ende des Vorgangs nicht mehr zurückgegeben. zu diesem Zeitpunkt gibt das System den Speicher frei.

> [!Note]  
> Das Momentaufnahme handle verhält sich wie ein Datei Handle und unterliegt den gleichen Regeln bezüglich der Prozesse und Threads, in denen es verwendet werden kann. Um anzugeben, dass das Handle vererbbar ist, erstellen Sie die Momentaufnahme mithilfe des **TH32CS \_ erben** -Werts.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Momentaufnahmen und Anzeigen von Prozessen](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 