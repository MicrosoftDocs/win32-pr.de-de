---
description: AVI Mux-Filter
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: AVI Mux-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f923ed944781bbaa36179b02db9022f38fc98ff6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478636"
---
# <a name="avi-mux-filter"></a>AVI Mux-Filter

Der AVI Mux-Filter akzeptiert mehrere Eingabestreams und überlagert sie im AVI-Format. Der Filter verwendet separate Eingabepins für jeden Eingabestream und einen Ausgabepin für den AVI-Stream.

Videoerfassungs- oder -erstellungsanwendungen können diesen Filter verwenden, um Dateien im AVI-Format auf dem Datenträger zu speichern. Der Filter ist in der Regel mit dem [File Writer-Filter](file-writer-filter.md) verbunden, kann jedoch eine Verbindung mit jedem Filter herstellen, dessen Eingabepin die IStream- und [**IMemInputPin-Schnittstellen**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) unterstützt.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages | | Eingabepin-Medientypen | Jeder Haupttyp, der einem FOURCC-Format im alten Stil entspricht, oder MEDIATYPE_AUXLine21Data. (Weitere Informationen finden Sie unter <a href="fourccmap.md"><strong>FOURCCMap-Klasse</strong></a>.)<ul><li>Wenn der Haupttyp MEDIATYPE_Audio ist, muss das Format FORMAT_WaveFormatEx.</li><li>Wenn der Haupttyp MEDIATYPE_Video ist, muss das Format FORMAT_VideoInfo oder FORMAT_DvInfo.</li><li>Wenn der Haupttyp MEDIATYPE_Interleaved ist, muss das Format FORMAT_DvInfo.</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Ausgabepin-Medientypen | MEDIATYPE_Stream, MEDIASUBTYPE_Avi | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| CLSID_AviDest | | CLSID-Eigenschaftsseite | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | | Ausführbare | qcap.dll | | <a href="merit.md">Leistungs-|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Hinweise

In den folgenden Anmerkungen werden verschiedene Aspekte der Funktionalität des AVI Mux-Filters beschrieben.

Pins

Wenn der AVI Mux-Filter erstellt wird, verfügt er über einen Eingabepin. Wenn jeder Eingabepin verbunden ist, erstellt der Filter einen neuen Eingabepin.

Streameigenschaften

Die Eingabepins unterstützen die IPropertyBag-Schnittstelle zum Festlegen von Eigenschaften für einzelne Streams. Derzeit ist die folgende Eigenschaft definiert:



| Eigenschaft | BESCHREIBUNG                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Der Name des Datenstroms. Diese Eigenschaft wird als Block `'strn'` geschrieben. |



 

Wenn der Filter ausgeführt wird oder angehalten wird, gibt die IPropertyBag::Write-Methode VFW \_ E \_ WRONG STATE \_ zurück.

Frameraten

Wenn der Upstreamfilter keine Bildfrequenz im **AvgTimePerFrame-Element** der [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ansteuert, verwendet der AVI Mux die Zeitstempel auf dem ersten Videoframe. Das AVI-Dateiformat unterstützt keine variablen Frameraten.

Gelöschte Frames

Der AVI Mux-Filter berechnet gelöschte Frames basierend auf den Medienzeiten der einzelnen Stichproben, sofern verfügbar, oder auf den Zeitstempeln der Stichprobe. Es schreibt einen Indexeintrag der Länge 0 (null) für jeden gelöschten Frame.

IMediaSeeking

Der AVI Mux-Filter implementiert die [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) wie folgt:

-   Die [**GetCurrentPosition-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) gibt den aktuellen Fortschritt des Multiplexings zurück. Wenn Sie eine Datei transcodieren (langsamer als in Echtzeit), ist dieser Wert genauer als der Wert, der vom Filter Graph Manager zurückgegeben wird. Weitere Informationen finden Sie im Abschnitt "Hinweise" der Referenzseite zu GetCurrentPosition.
-   Die [**GetDuration-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) fragt jeden Upstreamfilter ab und gibt die Dauer des längsten Streams zurück. Wenn einer dieser Filter den GetDuration-Aufruf fehlschlägt (oder IMediaSeeking nicht unterstützt), gibt DER AVI Mux einen Fehlercode zurück und füllt den *pDuration-Parameter* mit der längsten gefundenen Dauer aus. In diesem Fall ist *der Wert von pDuration* jedoch nicht notwendigerweise die Länge des längsten Eingabestreams.
-   Der AVI Mux implementiert nicht die Methoden GetStopPosition, GetPositions, GetAvailable, GetRate oder GetPreroll. und implementiert auch keine \* Set-Methoden für Suchmethoden.

AVI 2.0-Dateiformaterweiterungen

DirectShow unterstützt derzeit die folgenden AVI 2.0-Dateiformaterweiterungen:

-   Höhere GRÖßE der AVI-Datei (größer als 1 GB)
-   Hierarchische Indizierung

Weitere Informationen finden Sie in Version 1.02 der OpenDML AVI-Dateiformaterweiterungen, die im OpenDML AVI M-JPEG File Format Subcommittee veröffentlicht wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



