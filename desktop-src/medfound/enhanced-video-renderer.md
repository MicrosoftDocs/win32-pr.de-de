---
description: Der Enhanced Video Renderer (EVR) ist eine Komponente, die ein Video zum Monitor "Users" anzeigt.
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: Erweiterter Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342489"
---
# <a name="enhanced-video-renderer"></a>Erweiterter Videorenderer

Der Enhanced Video Renderer (EVR) ist eine Komponente, die ein Video zum Benutzer Monitor anzeigt. Es gibt zwei Versionen des EVR:

-   Die EVR-Medien Senke für Media Foundation Anwendungen.
-   Der EVR-Filter für DirectShow-Anwendungen.

Beide Versionen verwenden dieselben internen Objekte zum Rendering von Videos, und Sie nutzen viele der gleichen Schnittstellen gemeinsam.

Der EVR kann bis zu 16 Videostreams mischen. Der erste Eingabedaten Strom wird als *Verweis Datenstrom* bezeichnet. Der Verweis Datenstrom wird immer zuerst in der z-Reihenfolge angezeigt. Alle zusätzlichen Streams werden als *Substreams* bezeichnet und werden oberhalb des Verweis Datenstroms gemischt. Die Anwendung kann die z-Reihenfolge der untergeordneten Datenströme ändern, aber kein untergeordneter Stream kann in der z-Reihenfolge angegeben werden.

Der Grafiktreiber bestimmt, welche Videoformate unterstützt werden, aber in der Regel sind Sie auf Folgendes beschränkt:

-   Verweis Datenstrom: progressiv oder Zeilen Sprung-YUV ohne pro Pixel Alpha (z. b. NV12 oder im YUY2); oder progressiv RGB.
-   Unter Ströme: Progressive YUV mit pro Pixel-Alpha, wie z. b. ayuv oder AI44.

Die verfügbaren substreamformate können vom Format des Verweis Datenstroms abhängen. Weitere Informationen finden Sie unter [EVR Medientyp Aushandlung](evr-media-type-negotiation.md).

Intern verwendet der EVR ein Objekt mit dem Namen " *Mixer* ", um die Frames aus den Eingabedaten strömen zum Rendern auf eine Oberfläche zusammenzusetzen. Der Mixer führt auch Deinterlacing und Farbkorrektur aus. Die Ausgabe des Mischers ist der letzte zusammengesetzte Videoframe. Ein zweites Objekt, das als *Presenter* bezeichnet wird, rendert den Videoframe in der Anzeige. Der Presenter plant, wenn die Frames gerendert und das Direct3D-Gerät verwaltet werden. Eine Anwendung kann eine benutzerdefinierte Implementierung von "Mixer" oder "Presenter" bereitstellen.

Die Ausgabe Frame Rate ist an den Verweisstream gebunden. Jedes Mal, wenn die unter Ströme neue Frames empfangen, hält der Mixer auf diesen. Wenn der Verweis Datenstrom einen neuen Frame empfängt, wird dieser Frame vom Mixer mit den substreamframes in eine Verbundstruktur integriert. (Wenn der Verweis Datenstrom mit Zeilen Sprung verknüpft ist, ist für einen kompletten Referenzrahmen möglicherweise mehr als ein Medien Beispiel erforderlich.) Es ist möglich, dass ein untergeordneter Stream mehr als einen Frame empfängt, während der Mixer auf einen Referenzrahmen wartet. In diesem Fall verwirft der Mixer einfach den vorherigen substreamframe.

Da der Presenter das Direct3D-Gerät erstellt, ist es auch dafür verantwortlich, das Gerät mit anderen Pipeline Objekten zu teilen, die auf die DXVA-Dienste (DirectX Video Acceleration) zugreifen müssen. Insbesondere verwendet der EVR-Mixer die DXVA-Video Verarbeitungsdienste, um das Video zu deinstalmennen und zu mischen. Außerhalb des EVR können Software Decoder DXVA für die beschleunigte Video Decodierung verwenden. Der Presenter gibt das Direct3D-Gerät mithilfe des [Direct3D-Device Manager](direct3d-device-manager.md)aus. Das folgende Diagramm zeigt die interne Architektur des EVR. (Der in grau schattierte Software Decoder gehört nicht zum EVR.)

![Architektur Diagramm, das den EVR anzeigt.](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>EVR-Schnittstellen

Der EVR unterstützt die folgenden Schnittstellen. Einige dieser Schnittstellen werden vom Mixer oder der Presenter implementiert. Das Referenz Thema beschreibt für jede Schnittstelle, wie ein Zeiger auf die-Schnittstelle zu erhalten ist.

| Schnittstelle                                                    | BESCHREIBUNG                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Ievrfilterconfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | Legt die Anzahl der Eingabe Pins für den EVR-Filter fest (nur DirectShow).                                |
| [**Ievrfilterconfigex**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | Konfiguriert den EVR-Filter (nur DirectShow).                                                      |
| [**Ievrtreuhändvideoplugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | Aktiviert ein EVR-Plug-in zum Rendering von geschütztem Video.                                                 |
| [**IMF-redsample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | Ermöglicht es dem EVR Presenter, einen bestimmten Frame vom Mixer anzufordern.                             |
| [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | Ermöglicht dem Quality Manager das Anpassen der EVR-Videoqualität.                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | Ermöglicht es einem benutzerdefinierten Mixer oder Presenter, Schnittstellen Zeiger aus dem EVR zu erhalten.                       |
| [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | Gibt den Geräte Bezeichner eines EVR-Mischers oder-Präsentators zurück.                                       |
| [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | Steuert, wie das EVR Video anzeigt.                                                              |
| [**IMF videomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alpha: kombiniert ein statisches Bitmapbild mit dem Video.                                                |
| [**IMF videomixercontrol**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | Steuert, wie der erweiterte Videorenderer (EVR) Video-unter Ströme mischt.                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | Steuert die Einstellungen für Video Deinterlacing.                                                     |
| [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | Ordnet eine Position in einem Eingabe-Videodaten Strom der entsprechenden Position in einem ausgabevideostream zu. |
| [**IMF videopresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | Verfügbar gemacht von der EVR Presenter.                                                                     |
| [**IMF videoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | Steuert die Videoverarbeitung, einschließlich Anpassungen, Rausch Filtern und Detail Filtern.               |
| [**Imsvideorenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | Legt einen Mixer oder einen Presenter auf dem EVR fest.                                                             |
| [**IMF videosamplezuordcator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | Weist Videobeispiele zu.                                                                          |



 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                    | BESCHREIBUNG                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Verwenden des DirectShow-EVR-Filters](using-the-directshow-evr-filter.md)   | Wie Sie den EVR in einer DirectShow-Anwendung verwenden.                                       |
| [Verwenden der EVR-Medien Senke](using-the-evr-media-sink.md)                 | Wie Sie den EVR in einer Media Foundation-Anwendung verwenden.                                 |
| [Verwenden der Video Anzeige Steuerelemente](using-the-video-display-controls.md) | Steuern der Art und Weise, wie das EVR Video im Anwendungsfenster anzeigt. |
| [Verwenden der Video-Mixer-Steuerelemente](using-the-video-mixer-controls.md)     | Steuern der Art und Weise, wie der EVR-Mixer funktioniert.                               |
| [EVR-Medientyp Aushandlung](evr-media-type-negotiation.md)             | Beschreibt, wie der EVR bestimmt, welche Videoformate er als Eingabe annehmen kann.          |
| [Benutzerdefinierte Mixer](custom-mixers.md)                                       | Erfahren Sie, wie Sie einen benutzerdefinierten Mixer für den EVR schreiben.                                              |
| [Schreiben von EVR Presenter](how-to-write-an-evr-presenter.md)       | Erfahren Sie, wie Sie einen benutzerdefinierten Presenter für den EVR schreiben.                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



