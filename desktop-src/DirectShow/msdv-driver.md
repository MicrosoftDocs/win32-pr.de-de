---
description: MSDV-Treiber
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: MSDV-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748620"
---
# <a name="msdv-driver"></a>MSDV-Treiber

MSDV ist der WDM-Treiber (Microsoft Windows Driver Model) für DV-Dvds. Der Treiber wird als DirectShow-Filter angezeigt, wenn das Gerät angeschlossen ist. Sie wird in zwei Filterkategorien aufgeführt:

-   CLSID \_ VideoInputDeviceCategory ("Video Capture Sources")
-   AM \_ KSCATEGORY \_ RENDER ("WDM Streaming Rendering Devices")

Der Anzeigename des Filters ist `Microsoft DV Camera and VCR` oder eine lokalisierte Entsprechung. Auf einigen Geräten enthält die **Description-Eigenschaft** eine Beschreibung des spezifischen Modells, das anstelle des generischen Anzeigenamens verwendet werden kann. Weitere Informationen finden Sie unter [Auswählen eines Erfassungsgeräts.](selecting-a-capture-device.md)

MSDV verfügt über zwei Ausgabepins. Ein Pin stellt DV-Frames bereit, die überlappende Audio- und Videodaten enthalten. Die andere Stecknadel stellt nur Videoframes ohne Audio bereit. MSDV kann nicht gleichzeitig von beiden Pins streamen, sodass jeweils nur ein Ausgabepin verbunden werden kann. Weitere Informationen zum Erfassen von Videos von einem DV-Gerät finden Sie unter [Capture DV to File](capture-dv-to-file.md).

![Erfassen von DV-Daten vom Gerät](images/dv-filters4.png)

Die meisten DV-Datenträger verfügen über eine VTR-Untereinheit (Video Tape Recorder), die Daten vom Band auf den Computer übertragen kann. Für die Anwendung funktioniert die Erfassung über Band genauso wie die Erfassung von Livevideos. Der einzige Unterschied besteht darin, dass die Anwendung den externen Bandtransport steuern muss – Starten und Beenden des Bandes, Zurückspulen usw. Zu diesem Zweck macht MSDV die Schnittstellen [**IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)und [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) verfügbar. Weitere Informationen zum Steuern eines VTR finden Sie unter [Steuern eines DV-Cameras.](controlling-a-dv-camcorder.md)

Sie können dv auch vom Computer an den -Laptop übertragen. Das Video kann dann auf dem Onboardingbildschirm des Bands angezeigt oder auf Band aufgezeichnet werden. Zur Unterstützung dieser Funktionalität verfügt MSDV über einen Eingabepin, der einen überlappende DV-Datenstrom empfangen kann. Wenn der Eingabepin verbunden ist, fungiert MSDV als Rendererfilter anstelle eines Erfassungsfilters. MSDV unterstützt keine Suche in diesem Modus. Weitere Informationen zum Senden von DV an das Gerät finden Sie unter [Übertragen von DV von Datei zu Band.](transmit-dv-from-file-to-tape.md)

![Übertragen von DV-Daten an das Gerät](images/dv-filters5.png)

Beachten Sie, dass die Ein- und Ausgabepins nicht gleichzeitig verbunden werden können, da das Gerät nicht gleichzeitig in beide Richtungen streamen kann.

In vielen Modi führt der Wechsel zwischen VTR-Modus und Kameramodus dazu, dass das Gerät ausgeschaltet wird. Daher kann DirectShow das Gerät verlieren, wenn der Benutzer den Modus wechselt. Informationen zu Ereignissen zum Entfernen von Geräten finden Sie unter [Benachrichtigung zum Entfernen von Geräten.](device-removal-notification.md)

## <a name="remarks"></a>Hinweise

Informationen dazu, welche DV-Formate vom MSDV-Treiber unterstützt werden, finden Sie unter [**DV Video-Untertypen.**](dv-video-subtypes.md)

Einige Tipps zum Erstellen von Filterdiagrammen mit MSDV:

-   Sie können [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) nicht verwenden, um einen Ausgabepin auf MSDV zu rendern. (Der Filter-Graph-Manager versucht, den Ausgabepin mit dem Eingabepin von MSDV zu verbinden, wodurch ein Fehler auftritt.) Verwenden Sie stattdessen [**IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) oder [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Wenn ein Filterdiagramm MSDV enthält, sollte MSDV die Referenzuhr für das Diagramm bereitstellen. Ab DirectX 8.0 wählt der Filter Graph Manager automatisch MSDV als Referenzuhr aus. Bei früheren Versionen sollten Sie die [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) im Filter Graph-Manager aufrufen. Weitere Informationen zu Uhren finden Sie unter [Zeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)
-   Je nach Gerät können einige Methoden in **IAMExtDevice,** **IAMExtTransport** und **IAMTimeCodeReader** Windows Fehlercodes anstelle von **HRESULT-Werten** zurückgeben. Mögliche Fehlercodes sind:

    | Fehlercode              | BESCHREIBUNG                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | \_FEHLERTIMEOUT          | Bei einem Befehl für ein externes Gerät ist ein Time out aufgetreten.                                                        |
    | FEHLER \_ REQ \_ NOT \_ ACCEP  | Das Gerät hat diesen externen Gerätebefehl nicht akzeptiert.                                          |
    | FEHLER \_ NICHT \_ UNTERSTÜTZT   | Das Gerät unterstützt diesen externen Gerätebefehl nicht.                                        |
    | FEHLERANFORDERUNG \_ \_ ABGEBROCHEN | Ein externer Gerätebefehl wurde abgebrochen. Möglicherweise wurde das Gerät entfernt, oder es wurde ein Bus zurückgesetzt. |

    

     

### <a name="device-information"></a>Geräteinformationen

In Windows Edition und Windows XP unterstützt der Gerätemoniker des DV-Filters zusätzlich zur **FriendlyName-Eigenschaft** eine **Description-Eigenschaft.** Diese Eigenschaft gibt eine Beschreibung des Geräts aus der INF-Datei zurück, die in der Regel den Markennamen des Geräts enthält. Diese Eigenschaft wird jedoch nicht für alle Gerätemodelle unterstützt.

Weitere Informationen zu Gerätemonikern finden Sie unter [Verwenden des Systemgeräte-Enumerators.](using-the-system-device-enumerator.md)

### <a name="clock-times"></a>Uhrzeiten

Der MSDV-Treiber verwendet die 1394-Busuhr, die in den 1394-Datenpaketen enthalten ist, um die Uhr abzuleiten. Diese Werte werden verwendet, um die DV-Medienbeispiele mit einem Zeitstempel zu versehen. Da es sich bei dieser Quelluhr nicht um die Uhr des Computersystems handelt, werden die Zeiten letztendlich von der Uhr des Computersystems abweichen. Wie bereits erwähnt, wählt der Filter Graph Manager jedoch standardmäßig MSDV als Graphverweisuhr aus.

Die [**IAMDroppedFrames-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) meldet das aktuelle Measure des Treibers für gelöschte Frames. Dieser Wert ist möglicherweise nicht perfekt mit der tatsächlichen Anzahl gelöschter Frames zu einem bestimmten Zeitpunkt synchronisiert. Wenn Frames gelöscht werden, gibt dies an, dass das System nicht ausgeglichen ist (die Datenproduktion überschreitet den Datenverbrauch). Beispielsweise ist die Festplatte des Benutzers möglicherweise nicht schnell genug, um DV-Erfassungsraten zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



