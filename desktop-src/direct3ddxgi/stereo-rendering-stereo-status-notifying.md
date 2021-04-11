---
description: Apps können nur dann in Stereo dargestellt werden, wenn das Betriebssystem anzeigt, dass Sie das Verhalten der Stereoskopie in 3D aktivieren. Apps legen fest, ob Sie in stereoskopischen 3D-Daten unterschiedlich gerostet werden, je nachdem, ob Sie sich im Fenster
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Rendering in Stereo und Benachrichtigung über den Stereo Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123326"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Rendering in Stereo und Benachrichtigung über den Stereo Status

Apps können nur dann in Stereo dargestellt werden, wenn das Betriebssystem anzeigt, dass Sie das Verhalten der Stereoskopie in 3D aktivieren. Apps legen fest, ob Sie in stereoskopischen 3D-Daten unterschiedlich gerostet werden, je nachdem, ob Sie sich im Fenster

Eine Fenster Anwendung ruft die [**IDXGIFactory2:: iswindowedstereoaktivierte**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) Methode auf, um zu bestimmen, ob Sie in Stereo dargestellt werden soll. Eine voll Bild-App Ruft die [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) -Methode auf und bestimmt dann, ob einer der zurückgegebenen Anzeigemodi das Rendern in Stereo unterstützt. Die **GetDisplayModeList1** -Methode listet keine Stereo Modi auf, es sei denn, Sie geben das Stereo-Flag der [**DXGI-enumerationsmodi \_ \_ \_**](dxgi-enum-modes.md) im *Flags* -Parameter an. Ein Fenster oder eine voll Bild-APP, das Stereo zuerst unterstützt, macht die Entscheidung, basierend auf einem Rückruf der **IDXGIFactory2:: iswindowedstereoaktivierten** Methode oder der **IDXGIOutput1:: GetDisplayModeList1** -Methode in Stereo dargestellt zu werden, und registriert sich dann für Benachrichtigungen über die Änderungen des Stereo-Status. Da die APP sich nicht auf die Benachrichtigung verlassen kann, um den aktuellen Status des stereoskopischen 3D-Anzeige Verhaltens anzugeben, muss beim Empfang eines Benachrichtigungs Ereignisses oder einer Fenster Meldung entweder **IDXGIFactory2:: iswindowedstereoaktivierte** oder **IDXGIOutput1:: GetDisplayModeList1** erneut aufgerufen werden, um den aktuellen Status des stereoskopischen 3D-Anzeige Verhaltens des Betriebssystems zu ermitteln.

Wenn Sie in Stereo Renderinginformationen erstellen möchten, müssen Sie sich für Stereo Benachrichtigungen registrieren. Eine APP kann sich registrieren, um über eine Meldung an ein Fenster oder durch Ereignis Signalisierung benachrichtigt zu werden. Um sich zu registrieren, um Benachrichtigungs Meldungen in einem Fenster zu den Stereo Statusänderungen zu empfangen, ruft eine APP die [**IDXGIFactory2:: registerstereostatuswindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) -Methode auf. Um sich zu registrieren, um Benachrichtigungen über den Wechsel von Stereo-Status über Ereignis Signalisierung zu erhalten, ruft eine APP die [**IDXGIFactory2:: registerstereostatusevent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) -Methode auf. Beide Methoden geben einen Zeiger auf einen Schlüsselwert zurück, der von der APP zum Aufheben der Registrierung der Benachrichtigung verwendet werden kann. Um die Registrierung der Benachrichtigung aufzuheben, übergibt die APP diesen Schlüsselwert an die [**IDXGIFactory2:: unregisterstereostatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) -Methode.

Der Stereo-Status kann die folgenden Elemente enthalten:

-   Die Benutzerkonfiguration.

    Windows-Benutzer können die Stereo Anzeige in den Anzeigeeinstellungen der Systemsteuerung in den Einstellungen der Systemsteuerung aktivieren oder deaktivieren.

-   Die Funktion und Konfiguration des Computers, einschließlich Grafikadapter, Grafiktreiber und Monitor Einrichtung.

Das [Beispiel "Direct3D 11,1 Simple Stereo 3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) " zeigt, wie ein Stereotyp der 3D-Anwendung hinzugefügt wird und wie auf System Stereo Änderungen reagiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
