---
description: Benutzerdefinierte Mixer
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Benutzerdefinierte Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344639"
---
# <a name="custom-mixers"></a>Benutzerdefinierte Mixer

In diesem Thema wird beschrieben, wie ein benutzerdefinierter Mixer für den erweiterten Videorenderer (EVR) geschrieben wird. Sie können einen benutzerdefinierten Mixer entweder mit der Media Foundation EVR-Medien Senke oder mit dem DirectShow-EVR-Filter verwenden. Weitere Informationen zu Mixern und Moderatoren finden Sie unter [Enhanced Video Renderer](enhanced-video-renderer.md).

Der Mixer ist eine Media Foundation Transformation (MFT) mit einer oder mehreren Eingaben (dem Verweis Datenstrom und den unter strömen) und einer Ausgabe. Der Eingabestream empfängt Beispiele von Upstream. Der Ausgabestream liefert Beispiele für den Presenter. Der EVR ist für das Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) im Mixer zuständig, und der Presenter ist für das Aufrufen von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)verantwortlich.

Ein EVR-Mixer muss mindestens die folgenden Schnittstellen implementieren:



| Schnittstelle                                                                | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Stellt grundlegende MFT-Funktionen bereit.                                                                 |
| [**Imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Ermöglicht dem Mixer, Schnittstellen vom EVR zu erhalten.                                                |
| [**IMF videoabviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Ermöglicht dem Mixer, Schnittstellen vom EVR zu erhalten.                                                |
| [**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Wird verwendet, um das [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) -Attribut für den EVR verfügbar zu machen. |



 

Optional kann eine MFT eine der folgenden Schnittstellen implementieren:



| Schnittstelle                                                | BESCHREIBUNG                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ievrtreuhändvideoplugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Erforderlich, um geschützte Inhalte wiederzugeben.                                                                                                                  |
| [**IMF-Dienst**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Macht Schnittstellen wie [**imfvideomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) und [**imfvideoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) für die Anwendung verfügbar. |
| [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Ermöglicht dem Quality Manager das Anpassen der Videoqualität.                                                                                             |
| [**IMF videomixerbitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Ermöglicht der Anwendung, eine statische Bitmap auf das Video zu mischen.                                                                                       |
| [**IMF videopositionmapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Ordnet die Koordinaten im Video Frame der Ausgabe den Koordinaten des eingabevideoframes zu.                                                                  |
| [**IMF videoprocessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Macht einige DXVA-Video Verarbeitungs Features für die Anwendung verfügbar.                                                                                      |



 

Die Format Aushandlung mit dem Mixer funktioniert wie folgt:

1.  Der EVR legt den Medientyp für den Verweis Datenstrom fest.
2.  Der EVR ruft [**IMF videopresenter::P rocess Message**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) für den Presenter mit der Meldung " **\_ \_ invalidatemediatype" der MF-Nachricht** auf.

3.  Der Presenter legt den Medientyp für den Ausgabestream des Mischers fest.
4.  Der EVR legt den Medientyp für die untergeordneten Datenströme fest.

Wenn sich der Medientyp im Verweis Datenstrom ändert, sind die anderen Medientypen des Mixers nicht mehr gültig. Die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers schlägt dann fehl und gibt die Änderung von MF-E-Stream-Daten **\_ \_ \_ Strom \_** zurück. Der Presenter sollte an dieser Stelle nichts Unternehmen. Der EVR initiiert den formataushandlungs Prozess erneut.

Wenn ein Eingabedaten Strom das Ende des Streams erreicht, ruft der EVR [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) auf dem Mixer mit dem [**\_ \_ \_ Ende \_ des Daten \_ Stroms der MFT-Nachrichten Benachrichtigung**](mft-message-notify-end-of-stream.md)auf.

Der Mixer sendet die folgenden Ereignisse mithilfe der [**imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) -Schnittstelle von EVR an den EVR. Diese Schnittstelle ist in der DirectShow SDK-Dokumentation dokumentiert.



| Ereignis                                            | BESCHREIBUNG                            |
|--------------------------------------------------|----------------------------------------|
| [**EC- \_ Beispiel \_ erforderlich**](../directshow/ec-sample-needed.md) | Für den Mixer ist ein neues Eingabe Beispiel erforderlich. |



 

Der EVR könnte [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf dem Mixer aufzurufen, bevor das Streaming gestartet wird. Der Mixer sollte diese Aufrufe nicht fehlschlagen. Stattdessen sollte die Ausgabe Oberfläche in schwarze Pixel gefüllt werden. Der Mixer sollte weiterhin Ausgabe Beispiele mit Farben füllen, bis er eine Nachricht zum [**\_ \_ \_ Starten \_ von MFT**](mft-message-notify-begin-streaming.md) -Nachrichten empfängt oder die [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode aufgerufen wird. Wenn der Mixer eine Nachricht zum [**\_ \_ \_ Beenden \_ von MFT**](mft-message-notify-end-streaming.md) -Nachrichten empfängt, sollte er wieder in den farbfüllmodus wechseln.

## <a name="implementing-imfvideodeviceid"></a>Implementieren von IMF videode viceid

Die [**IMF videodeviceid**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) -Schnittstelle enthält eine Methode, [**getdeviceid**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), die eine Geräte-GUID zurückgibt. Die Geräte-GUID stellt sicher, dass der Presenter und der Mixer kompatible Technologien verwenden. Wenn die Geräte-GUIDs nicht stimmen, kann der EVR nicht initialisiert werden.

Der Standard-Mixer und der Presenter verwenden jeweils Direct3D 9, wobei die Geräte-GUID IID \_ IDirect3DDevice9 entspricht. Wenn Sie beabsichtigen, den benutzerdefinierten Presenter mit dem Standard-Mixer zu verwenden, muss die Geräte-GUID des Presenter IID \_ IDirect3DDevice9 lauten. Wenn Sie beide Komponenten ersetzen, können Sie eine neue Geräte-GUID definieren.

## <a name="implementing-imftopologyservicelookupclient"></a>Implementieren von imftopologyservicelookupclient

Der Mixer muss die [**imftopologyservicelookupclient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) -Schnittstelle implementieren. Bevor das Streaming beginnt, ruft der EVR [**imftopologyservicelookupclient:: initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) auf und übergibt einen Zeiger auf die [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) -Schnittstelle von EVR. Der Mixer verwendet diesen Zeiger, um Schnittstellen Zeiger aus dem EVR zu erhalten.

Der Mixer muss mindestens die folgende Schnittstelle Abfragen:

-   [**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Wenn der EVR [**imftopologyservicelookupclient:: releaseservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers)aufruft, muss der Mixer alle vom Aufruf von [**initservicepointer**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)abgerufenen Zeiger freigeben.

## <a name="mixer-attributes"></a>Mixattribute

Ein Mixer sollte die folgenden Attribute unterstützen.



| Attribut                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md)                          | Gibt an, ob der Mixer eine DirectX-Video Beschleunigung (DXVA) unterstützt.                                                                                                                                                                               |
| [**\_ \_ Anzahl erforderlicher MF-Anforderungen \_ \_**](mf-sa-required-sample-count-attribute.md) | Die Anzahl der Videobeispiele, die der EVR für jeden mixerstream zuordnen soll. Dieses Attribut gilt für einzelne Streams. Verwenden Sie den Attribut Speicher, der von [**IMF Transform:: getinputstreamattribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)zurückgegeben wurde. |



 

## <a name="setting-the-mixer-on-the-evr"></a>Festlegen des Mischers auf dem EVR

Um einen benutzerdefinierten Mixer für den EVR festzulegen, nennen Sie [**imfvideorenderer:: initializerenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). Sowohl der DirectShow-EVR-Filter als auch die EVR-Medien Senke implementieren diese Methode.

**EVR-Aktivierungs Objekt**. Wenn Sie das EVR-Aktivierungs Objekt verwenden, können Sie einen benutzerdefinierten Mixer bereitstellen, indem Sie eines der folgenden Attribute für das EVR-Aktivierungs Objekt festlegen:



| Attribut                                                                                                 | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**MF Aktivieren des \_ \_ benutzerdefinierten \_ Video \_ Mischers \_ aktivieren**](mf-activate-custom-video-mixer-activate-attribute.md) | Zeiger auf ein Aktivierungs Objekt für den Mixer. Das Aktivierungs Objekt muss die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle implementieren. |
| [**MF \_ - \_ benutzerdefinierte \_ Video-Mixer- \_ \_ CLSID aktivieren**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID des Mischers.                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 
