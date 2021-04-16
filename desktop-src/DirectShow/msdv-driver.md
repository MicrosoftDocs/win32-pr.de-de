---
description: Msdv-Treiber
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Msdv-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7c1bda24980abe84a11613126476ccfe35380d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392361"
---
# <a name="msdv-driver"></a>Msdv-Treiber

Msdv ist der Microsoft Windows-Treibermodell (WDM)-Treiber für DV-Camcorders. Der Treiber wird als DirectShow-Filter angezeigt, wenn das Gerät angeschlossen ist. Es wird in zwei Filter Kategorien aufgezählt:

-   CLSID \_ videoinputabvicecategory ("Video Erfassungs Quellen")
-   AM \_ kscategory-Rendering \_ ("WDM-Streaminggeräte")

Der Anzeige Name des Filters ist `Microsoft DV Camera and VCR` oder eine lokalisierte Entsprechung. Bei manchen Geräten enthält die **Description** -Eigenschaft eine Beschreibung des jeweiligen Modells, das anstelle des generischen anzeigen Amens verwendet werden kann. Weitere Informationen finden Sie unter [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md).

Msdv verfügt über zwei Ausgabe Pins. Eine PIN liefert DV-Frames, die verschachtelte Audiodaten und Videodaten enthalten. Die andere PIN liefert nur-Video-Frames ohne Audiodaten. Msdv kann nicht gleichzeitig von beiden Pins gestreamt werden, sodass jeweils nur eine Ausgabe-PIN verbunden werden kann. Weitere Informationen zum Erfassen von Videos von einem DV-Gerät finden [Sie unter Erfassen von DV in Dateien](capture-dv-to-file.md).

![Erfassen von DV-Daten vom Gerät](images/dv-filters4.png)

Die meisten DV-Camcorder verfügen über eine VTR-Untereinheit (Video Tape Recorder), mit der Daten vom Band an den Computer übertragen werden können. Für die Anwendung funktioniert die Erfassung von Band genauso wie die Erfassung von Livevideos. Der einzige Unterschied besteht darin, dass die Anwendung den externen Band Transport Steuern muss – das Band starten und beenden, Zurückspulen usw. Zu diesem Zweck macht msdv die Schnittstellen [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)und [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) verfügbar. Weitere Informationen zum Steuern eines VTR finden Sie unter [Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md).

Sie können auch DV vom Computer an den Camcorder übertragen. Das Video kann dann auf dem Bildschirm zum Integrieren des Camcorders angezeigt oder auf Band aufgezeichnet werden. Um diese Funktionalität zu unterstützen, verfügt msdv über eine Eingabe-PIN, die einen verschachtelten DV-Stream empfangen kann. Wenn die Eingabe-PIN verbunden ist, fungiert msdv als rendererfilter anstelle eines Erfassungs Filters. Msdv unterstützt das Suchen in diesem Modus nicht. Weitere Informationen zum Senden von DV an das Gerät finden Sie unter über [tragen von DV von der Datei auf das Band](transmit-dv-from-file-to-tape.md).

![Übertragen von DV-Daten an das Gerät](images/dv-filters5.png)

Beachten Sie, dass die Eingabe-und Ausgabe Pins nicht gleichzeitig verbunden werden können, da das Gerät nicht gleichzeitig in beide Richtungen streamen kann.

In vielen Camcordern bewirkt das Wechseln zwischen dem VTR-Modus und dem Kameramodus, dass das Gerät ausgeschaltet wird. Daher kann DirectShow das Gerät verlieren, wenn der Benutzer den Modus wechselt. Informationen zu Geräte Entfernungs Ereignissen finden Sie unter [Benachrichtigung zum Entfernen](device-removal-notification.md)von Geräten.

## <a name="remarks"></a>Bemerkungen

Informationen dazu, welche DV-Formate vom msdv-Treiber unterstützt werden, finden Sie unter [**DV-Video Untertypen**](dv-video-subtypes.md).

Einige Tipps zum Entwickeln von Filter Diagrammen mit msdv:

-   Sie können [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) nicht verwenden, um eine Ausgabe-PIN auf msdv zu Rendering. (Der Filter Graph-Manager versucht, die Ausgabe-PIN mit der Eingabe-PIN von msdv zu verbinden, bei der ein Fehler auftritt.) Verwenden Sie stattdessen [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) oder [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Wenn ein Filter Diagramm msdv enthält, sollte msdv die Referenzuhr für das Diagramm bereitstellen. Ab DirectX 8,0 wählt der Filter Graph-Manager automatisch msdv als Referenzuhr aus. Bei früheren Versionen sollte die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode für den Filter Graph-Manager aufgerufen werden. Weitere Informationen zu Uhren finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).
-   Abhängig vom Gerät können einige Methoden in **IAMExtDevice**, **IAMExtTransport** und **IAMTimecodeReader** anstelle von **HRESULT** -Werten Windows-Fehlercodes zurückgeben. Folgende Fehlercodes sind möglich:

    | Fehlercode              | BESCHREIBUNG                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | Fehler \_ Timeout          | Timeout bei einem externen Geräte Befehl.                                                        |
    | Fehler beim Zurücksetzen des Fehlers. \_ \_ \_  | Das Gerät hat den Befehl "externer Gerät" nicht akzeptiert.                                          |
    | Fehler \_ nicht \_ unterstützt   | Der Befehl "externer Gerät" wird vom Gerät nicht unterstützt.                                        |
    | Fehler \_ Anforderung \_ abgebrochen | Ein externer Geräte Befehl wurde abgebrochen. Möglicherweise wurde das Gerät entfernt, oder es ist ein buszurücksetzen aufgetreten. |

    

     

### <a name="device-information"></a>Geräteinformationen

In der Windows Millennium Edition und Windows XP unterstützt der gerätermoniker des DV-Filters zusätzlich zur **FriendlyName** -Eigenschaft eine **Description** -Eigenschaft. Diese Eigenschaft gibt eine Beschreibung des Geräts aus der INF-Datei zurück, die in der Regel den Markennamen des Geräts enthält. Diese Eigenschaft wird jedoch nicht für alle Gerätemodelle unterstützt.

Weitere Informationen zu gerätermonikern finden [Sie unter Verwenden des System Geräte Enumerators](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Uhrzeiten

Der msdv-Treiber verwendet die 1394-busuhr, die in den 1394-Datenpaketen enthalten ist, um die Uhr abzuleiten. Diese Werte werden zum Zeitstempel der DV-Medien Beispiele verwendet. Da es sich bei dieser quelluhr nicht um die Systemuhr des Computers handelt, werden die Zeiten schließlich von der Computer Systemuhr abweichen. Wie bereits erwähnt, wählt der Filter Graph-Manager standardmäßig msdv als Diagramm-verweiszeit aus.

Die [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) -Schnittstelle meldet das aktuelle Measure von gelöschten Frames des Treibers. Dieser Wert wird möglicherweise nicht perfekt mit der tatsächlichen Anzahl der abgelegten Frames zu einem bestimmten Zeitpunkt synchronisiert. Wenn Frames abgelegt werden, gibt dies an, dass das System nicht ausgeglichen ist (die Datenproduktion überschreitet den Datenverbrauch). Beispielsweise ist die Festplatte des Benutzers möglicherweise nicht schnell genug, um die DV-Erfassungs Raten zu unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



