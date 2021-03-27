---
title: Befehlsliste
description: Eine Befehlsliste ist eine Sequenz von GPU-Befehlen, die aufgezeichnet und wiedergegeben werden können. Eine Befehlsliste kann die Leistung verbessern, indem der von der Laufzeit generierte Verwaltungsaufwand verringert wird.
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f8821645588ac7a9b48a4f6ce562c8c48cf96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711543"
---
# <a name="command-list"></a>Befehlsliste

Eine Befehlsliste ist eine Sequenz von GPU-Befehlen, die aufgezeichnet und wiedergegeben werden können. Eine Befehlsliste kann die Leistung verbessern, indem der von der Laufzeit generierte Verwaltungsaufwand verringert wird.

Verwenden Sie in den folgenden Szenarien eine Befehlsliste:

-   Rendersie in einem einzelnen Frame einen Teil der Szene in einem Thread, während ein anderer Teil der Szene in einem zweiten Thread aufgezeichnet wird. Geben Sie am Ende des Frames die aufgezeichnete Befehlsliste im ersten Thread wieder. Mit diesem Ansatz können Sie komplexe Renderingaufgaben über mehrere Threads oder Kerne hinweg skalieren.
-   Zeichnen Sie eine Befehlsliste vorab auf, bevor Sie Sie Rendering (z. b. beim Laden einer Ebene), und wiedergeben Sie Sie später in Ihrer Szene. Diese Optimierung funktioniert gut, wenn Sie etwas häufig Renderingvorgang durcharbeiten müssen.

Eine Befehlsliste ist unveränderlich und soll während einer einzelnen Ausführung einer Anwendung aufgezeichnet und wiedergegeben werden. Eine Befehlsliste ist nicht so konzipiert, dass Sie vor der Spiele Ausführung vorab aufgezeichnet und von ihren Medien geladen wird, da es keine Möglichkeit gibt, die Liste beizubehalten.

Eine Befehlsliste muss von einem verzögerten Kontext aufgezeichnet werden, Sie kann jedoch nur in einem unmittelbaren Kontext wiedergegeben werden. Verzögerte Kontexte können Befehlslisten gleichzeitig generieren.

-   Informationen zum Aufzeichnen einer Befehlsliste finden Sie unter Gewusst [wie: Aufzeichnen einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-record.md).
-   Weitere Informationen zur Wiedergabe einer Befehlsliste finden Sie unter Gewusst [wie: Wiedergeben einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-play.md).
-   Bei Verwendung einer Befehlsliste hängt die Leistung von der in einem Treiber implementierten Menge der Unterstützung ab. Informationen zum Überprüfen der Treiberunterstützung finden Sie unter Gewusst [wie: Überprüfen der Treiberunterstützung](overviews-direct3d-11-render-multi-thread-support.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




