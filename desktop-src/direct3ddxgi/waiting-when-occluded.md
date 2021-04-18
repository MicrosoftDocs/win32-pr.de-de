---
description: Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm unnötig ist (d. h., während Sie ausgeblendet werden).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Warten auf ein Ereignis, wenn das Rendering unnötig ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344310"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Warten auf ein Ereignis, wenn das Rendering unnötig ist

Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm unnötig ist (d. h., während Sie ausgeblendet werden). Wenn die Desktopfenster-Manager (DWM) oder eine APP synchronisiert werden, ist kein Rendering erforderlich, und das Betriebssystem kann für längere Zeit in niedrigeren Energiezuständen bleiben. Dies spart Strom und erweitert die Akku Lebensdauer.

Eine APP kann auf ein Ereignis warten, wenn Folgendes folgende Aktionen ausführen:

-   Alle Monitore sind deaktiviert.
-   Die Sitzung, in der die app ausgeführt wird, wird getrennt.
-   Die APP wird ausschließlich in einer einzigen Monitor Konfiguration im Vollbildmodus ausgeführt.
-   Die APP wird auf einem anderen Desktop als der aktive Desktop ausgeführt und verfügt nicht über die Berechtigung zum renderingzugriff auf dem aktiven Desktop.

Das Betriebssystem löst das Ereignis aus, wenn die APP wieder gereinigen werden kann. Das Ereignis wird während eines Treiber Upgrades oder einer TDR-Prozession (Timeout Erkennung und Wiederherstellung) nicht gelöscht, es wird jedoch gelöscht, wenn der neue Adapter und die Monitore aktiv werden.

Wenn Sie möchten, dass Ihre APP über Änderungen des Status der Okklusion benachrichtigt wird, muss sich die APP für diese Änderungen registrieren. Eine APP kann sich registrieren, um über Änderungen des Status der Okklusion über eine Nachricht an ein Fenster oder durch Ereignis Signalisierung benachrichtigt zu werden. Um sich zu registrieren, um Benachrichtigungs Statusänderungen an einem Fenster zu empfangen, ruft eine APP die [**IDXGIFactory2:: registeroksionstatuswindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) -Methode auf. Um sich zu registrieren, um Benachrichtigungen über die Statusänderungen der Okklusion per Ereignis Signalisierung zu empfangen, ruft eine APP die [**IDXGIFactory2:: registeroksionstatusevent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) -Methode auf. Beide Methoden geben einen Zeiger auf einen Schlüsselwert zurück, der von der APP zum Aufheben der Registrierung der Benachrichtigung verwendet werden kann. Um die Registrierung der Benachrichtigung aufzuheben, übergibt die APP diesen Schlüsselwert an die [**IDXGIFactory2:: unregisteroksionstatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



