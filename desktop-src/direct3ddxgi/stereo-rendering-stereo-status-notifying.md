---
description: Apps können nicht in Stereo gerendert werden, es sei denn, das Betriebssystem gibt an, dass das Stereo-3D-Anzeigeverhalten aktiviert wird. Apps bestimmen, ob in stereo-3D unterschiedlich gerendert werden soll, je nachdem, ob sie über ein Fenster oder einen Vollbildmodus angezeigt werden.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Rendern in Stereo und Benachrichtigen über den Stereostatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f17f324a884c5784c98a8f5c21ef9c9dac7b048fc72ae7ed0ea1a75e61e2551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987010"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Rendern in Stereo und Benachrichtigen über den Stereostatus

Apps können nicht in Stereo gerendert werden, es sei denn, das Betriebssystem gibt an, dass das Stereo-3D-Anzeigeverhalten aktiviert wird. Apps bestimmen, ob in stereo-3D unterschiedlich gerendert werden soll, je nachdem, ob sie über ein Fenster oder einen Vollbildmodus angezeigt werden.

Eine App mit Fenstern ruft die [**IDXGIFactory2::IsWindowedStereoEnabled-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) auf, um zu bestimmen, ob in Stereo gerendert werden soll. Eine Vollbild-App ruft die [**IDXGIOutput1::GetDisplayModeList1-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) auf und bestimmt dann, ob einer der zurückgegebenen Anzeigemodi rendering in Stereo unterstützt. Die **GetDisplayModeList1-Methode** listet keine Stereomodi auf, es sei denn, Sie geben das [**STEREO-Flag DXGI \_ ENUM \_ MODES \_**](dxgi-enum-modes.md) im *Flags-Parameter* an. Eine Fenster- oder Vollbild-App, die Stereo unterstützt, trifft zuerst die Entscheidung, in Stereo zu rendern, basierend auf einem Aufruf der **IDXGIFactory2::IsWindowedStereoEnabled-** bzw. **IDXGIOutput1::GetDisplayModeList1-Methode** und registriert sich dann für die Benachrichtigung über Stereostatusänderungen. Da sich die App nicht auf die Benachrichtigung verlassen kann, um den aktuellen Status des stereomodischen 3D-Anzeigeverhaltens anzugeben, muss sie beim Empfangen eines Benachrichtigungsereigniss oder einer Fenstermeldung entweder **IDXGIFactory2::IsWindowedStereoEnabled** oder **IDXGIOutput1::GetDisplayModeList1** erneut aufrufen, um den aktuellen Status des stereomodischen 3D-Anzeigeverhaltens des Betriebssystems zu bestimmen.

Wenn Sie in Stereo rendern möchten, müssen Sie sich für Stereobenachrichtigungen registrieren, um zu wissen, wann der Benutzer das Stereoverhalten deaktiviert oder aktiviert. Eine App kann sich registrieren, um über Stereo-3D-Statusänderungen über eine Nachricht in ein Fenster oder durch Ereignissignalisierung benachrichtigt zu werden. Eine App ruft die [**IDXGIFactory2::RegisterStereoStatusWindow-Methode**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) auf, um sich für den Empfang von Benachrichtigungsmeldungen an ein Fenster über Stereostatusänderungen zu registrieren. Um sich zu registrieren, um Benachrichtigungen über Stereostatusänderungen per Ereignissignalisierung zu erhalten, ruft eine App die [**IDXGIFactory2::RegisterStereoStatusEvent-Methode**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) auf. Beide Methoden geben einen Zeiger auf einen Schlüsselwert zurück, mit dem die App die Registrierung der Benachrichtigung aufheben kann. Zum Aufheben der Registrierung der Benachrichtigung übergibt die App diesen Schlüsselwert an die [**IDXGIFactory2::UnregisterStereoStatus-Methode.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)

Der Stereostatus kann die folgenden Elemente enthalten:

-   Die Benutzerkonfiguration.

    Windows Können Benutzer die Stereoanzeige mit der Option stereoaktiviertes 3D aktivieren im Systemsteuerung der Einstellungen.

-   Die Computerfunktion und -konfiguration, einschließlich Grafikadapter, Grafiktreiber und Monitoreinrichtung.

Im [Direct3D 11.1 Simple Stereo 3D Sample (Direct3D 11.1 Simple Stereo 3D Sample)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) wird gezeigt, wie sie einen stereo-ischen 3D-Effekt hinzufügen und auf Stereo-Systemänderungen reagieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1.2 Improvements](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
