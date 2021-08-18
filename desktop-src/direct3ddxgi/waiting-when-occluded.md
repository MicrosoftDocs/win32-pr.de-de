---
description: Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm nicht erforderlich ist (d. h., während sie verblendet sind).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Warten auf ein Ereignis, wenn das Rendering nicht erforderlich ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db1aa4805aa1dde25947ed25c90d14c9f3c2f4c8693d3599f1382937ee0dbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118517873"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Warten auf ein Ereignis, wenn das Rendering nicht erforderlich ist

Apps können auf ein Ereignis warten, wenn das Rendern auf dem Bildschirm nicht erforderlich ist (d. h., während sie verblendet sind). Wenn der Desktopfenster-Manager (DWM) oder eine App ver okkludent ist, ist kein Rendering erforderlich, und das Betriebssystem kann für längere Zeiträume in niedrigeren Leistungszuständen bleiben. Dies spart Strom und verlängert die Akkulebensdauer.

Eine App kann auf ein Ereignis warten, wenn:

-   Alle Monitore sind deaktiviert.
-   Die Sitzung, in der die App ausgeführt wird, wird getrennt.
-   Die App wird im Vollbildmodus ausschließlich auf einer einzelnen Monitorkonfiguration ausgeführt.
-   Die App wird auf einem anderen Desktop als der aktive Desktop ausgeführt und verfügt nicht über die Berechtigung zum Rendern auf dem aktiven Desktop.

Das Betriebssystem löst das -Ereignis aus, wenn die App wieder gerendert werden kann. Das Ereignis wird während eines Treiberupgrades oder einer TDR-Prozession (Timeout Detection and Recovery) nicht deaktiviert. Es wird jedoch deaktiviert, wenn der neue Adapter und die Monitore aktiv werden.

Wenn Sie möchten, dass Ihre App über Änderungen des Okklusionsstatus benachrichtigt wird, muss sich die App für diese Änderungen registrieren. Eine App kann sich registrieren, um über Änderungen des Okklusionsstatus über eine Nachricht an ein Fenster oder durch Ereignissignalisierung benachrichtigt zu werden. Eine App ruft die [**IDXGIFactory2::RegisterOcclusionStatusWindow-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) auf, um sich für den Empfang von Benachrichtigungsmeldungen in einem Fenster über Okklusionsstatusänderungen zu registrieren. Eine App ruft die [**IDXGIFactory2::RegisterOcclusionStatusEvent-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) auf, um sich zu registrieren, um Benachrichtigungen über Änderungen des Okklusionsstatus per Ereignissignalisierung zu erhalten. Beide Methoden geben einen Zeiger auf einen Schlüsselwert zurück, mit dem die App die Registrierung der Benachrichtigung aufheben kann. Zum Aufheben der Registrierung der Benachrichtigung übergibt die App diesen Schlüsselwert an die [**IDXGIFactory2::UnregisterOcclusionStatus-Methode.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1.2 Improvements](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



