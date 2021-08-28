---
title: Stichprobenerweiterungstypen
description: Stichprobenerweiterungstypen
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Medienformat-SDK, Beispielerweiterungen
- Advanced Systems Format (ASF), Beispielerweiterungen
- ASF (Advanced Systems Format), Beispielerweiterungen
- Windows Medienformat-SDK, Dateneinheitserweiterungen
- Advanced Systems Format (ASF), Dateneinheiterweiterungen
- ASF (Advanced Systems Format), Dateneinheiterweiterungen
- Windows Medienformat-SDK, Puffereigenschaften
- Advanced Systems Format (ASF), Puffereigenschaften
- ASF (Advanced Systems Format), Puffereigenschaften
- Beispielerweiterungen, Typen
- Dateneinheitenerweiterungen, Typen
- Puffereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1404dfee60c3de179df2bee0f7f123112002108
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479776"
---
# <a name="sample-extension-types"></a>Stichprobenerweiterungstypen

Beispielerweiterungen, auch als Dateneinheitserweiterungen (Data Unit Extensions, DUEs) oder Puffereigenschaften bezeichnet, sind Datenelemente, die an die Medienbeispiele im Datenabschnitt der ASF-Datei angefügt werden. Mehrere Arten von Beispielerweiterungen werden im Windows Media Format SDK definiert. Sie können auch eigene Erweiterungstypen erstellen.

Um Beispielerweiterungen zu verwenden, müssen Sie den Erweiterungstyp in den Datenstromkonfigurationsdaten des Profils identifizieren. Rufen Sie die [**IWMStreamConfig2::AddDataUnitExtension-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) auf, um einen Stream zum Akzeptieren von Beispielen mit erweiterten Daten zu konfigurieren.

Einzelne Beispielerweiterungen müssen den Eingabebeispielen durch Aufrufen der [**INSSBuffer3::SetProperty-Methode**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) hinzugefügt werden. Beim Lesen von Beispielen können Sie die [**INSSBuffer3::GetProperty-Methode**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) aufrufen, um die Erweiterungsdaten abzurufen. Sie können auch die Methoden der [**INSSBuffer4-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) verwenden, um die dateneinheitenerweiterungen aufzuzählen, die an ein Beispiel angefügt sind.

In der folgenden Tabelle sind die vordefinierten Bezeichner der Dateneinheitenerweiterung aufgeführt, und es werden die Daten beschrieben, die den jeweiligen Beispielen angefügt sind.




| Beispielerweiterungs-GUID | BESCHREIBUNG | 
|-----------------------|-------------|
| WM_SampleExtensionGUID_OutputCleanPoint | Die Daten geben an, ob das Beispiel ein <a href="wmformat-glossary.md"><em>Cleanpoint</em></a>ist. Der Wert 0 (null) gibt an, dass das Beispiel kein Cleanpoint ist. Ein Wert ungleich 0 (null) gibt an, dass es sich um einen Cleanpoint handelt. Dieser DUE-Typ (Sample Data Unit Extension) wird verwendet, um Cleanpoints beim Schreiben von vorkomprimierten Medienstreams nachzuverfolgen, die mit Codecs von Drittanbietern codiert wurden. | 
| WM_SampleExtensionGUID_Timecode | Die Daten sind eine <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> Struktur, die dem Beispiel zugeordnete SMPTE-Zeitcodedaten enthält. Die Größe für due ist immer WM_SampleExtension_Timecode_Size, also 14 Bytes.<br /> | 
| WM_SampleExtensionGUID_FileName | Diese Art von Beispielerweiterung wird für Dateistreams verwendet. Die Daten in einem Dateistreambeispiel sind ein Teil einer Datendatei. Die Daten in der Beispielerweiterung geben den Namen der Datei an, aus der der Inhalt des Beispiels entnommen wurde. Der Dateiname ist eine Zeichenfolge mit Breitzeichen, die den Dateinamen im Format name.extension ohne Pfadinformationen enthält.<br /> | 
| WM_SampleExtensionGUID_ContentType | Die Daten geben den Inhaltstyp an, der im Beispiel enthalten ist. Diese Art von Beispielerweiterung wird mit Videostreams mit Zeilensprung verwendet. Für alle Interlacinginhalte wird das flag WM_CT_INTERLACED verwendet, das durch ein bitweises <strong>OR</strong> mit WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST oder WM_CT_REPEAT_FIRST_FIELD kombiniert wird.<br /> Die Feldreihenfolge wird nicht im Codierungsprozess verwendet, sondern mit den komprimierten Stichproben beibehalten, sodass sie an die Renderinghardware übergeben werden kann. Durch das Wiedergeben von Inhalten mit der falschen Feldreihenfolge werden Artefakte wie Bewegungs-Jitter im Video eingeführt.<br /> Die Größe für diese DUE-Datei ist immer WM_SampleExtension_ContentType_Size.<br /> | 
| WM_SampleExtensionGUID_PixelAspectRatio | Die Daten geben das Pixel-Seitenverhältnis des Inhalts im Beispiel an. Dies gilt nur für Videos. Dieser Erweiterungstyp wird verwendet, um das Seitenverhältnis von nicht quadratischen Pixeln zu identifizieren. Weitere Informationen finden Sie unter So lesen und schreiben Sie <a href="to-read-and-write-video-streams-with-non-square-pixels.md">Video Streams mit nicht quadratischen Pixeln.</a><br /> Seitenverhältniswerte werden als Wort gespeichert, dessen unteres Byte der X-Aspekt und dessen hohes Byte der Y-Aspekt ist. Beispielsweise wird 16:9 als 0x0910 gespeichert.<br /> Die Größe für due ist immer WM_SampleExtension_PixelAspectRatio_Size, also 2 Byte.<br /> | 
| WM_SampleExtensionGUID_SampleDuration | Die Daten geben die Dauer des im Pufferobjekt enthaltenen Beispiels in Millisekunden an. Wenn bei der Wiedergabe due festgelegt ist, verwendet das Readerobjekt es, um den vorhandenen Wert für die Samplingdauer zu überschreiben. Diese DUE wird automatisch von den SDK-Laufzeitkomponenten in Videostreams mit Bitraten von 100 KBit/s oder höher festgelegt, wobei der Mehraufwand der DUE-Informationen nicht signifikant ist. Sie ist nicht für Streams mit Bitraten unter 100 KBit/s festgelegt. Anwendungen sollten diesen DUE nicht manuell festlegen, da der Writer (in Datenströmen mit hoher Bitrate) den Wert mit eigenen Daten überschreibt.<br /> Die Größe für due ist immer WM_SampleExtension_SampleDuration_Size, also 2 Byte.<br /> | 
| WM_SampleExtensionGUID_ChromaLocation | Die Daten geben den Typ des subsampling-Typs an, der im I420-Videoformat verwendet wird. Der Wert dieser Erweiterung wird auf einen der folgenden Werte festgelegt:<br /><ul><li>WM_CL_INTERLACED420</li><li>WM_CL_PROGRESSIVE420</li></ul>Diese Dateneinheitenerweiterung ist im Profil nicht konfiguriert. Sie ist in der Ausgabe von Beispielen des Decoders enthalten.<br /> Die Größe dieses DUE ist immer WM_SampleExtension_ChromaLocation_Size, also 1 Byte.<br /> | 
| WM_SampleExtensionGUID_ColorSpaceInfo | Die Daten enthalten Informationen zum Farbraum, der für den aktuellen Videoframe verwendet wird. Der Wert dieser Erweiterung <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong></strong></a> ist eine WMT_COLORSPACEINFO_EXTENSION_DATA-Struktur.<br /> Diese Dateneinheitenerweiterung ist im Profil nicht konfiguriert. Sie ist in der Ausgabe von Beispielen des Decoders enthalten.<br /> Die Größe dieses DUE-Werts ist immer WM_SampleExtension_ColorSpaceInfo_Size, also 3 Byte.<br /> | 
| WM_SampleExtensionGUID_UserDataInfo | Die Daten sind benutzerdefinierte Benutzerdaten. Die ersten vier Bytes der Daten enthalten die Größe der benutzerdefinierten Daten.<br /> Das nächste Byte enthält den Typ der Benutzerdaten, die in der Beispielerweiterung bereitgestellt werden. Die folgenden Typen werden unterstützt:<br /><ul><li>0x1F: Benutzerdaten auf Sequenzebene</li><li>0x1E: Benutzerdaten auf Einstiegspunktebene</li><li>0x1D: Benutzerdaten auf Frameebene</li><li>0x1C: Benutzerdaten auf Feldebene</li><li>0x1B : Sliceebenenbenutzerdaten</li></ul>Das sechste und nachfolgende Bytes enthalten die Benutzerdaten. Es gibt so viele Bytes von Benutzerdaten, wie durch die Zahl in den ersten vier Bytes angegeben.<br /> Diese Dateneinheitenerweiterung ist im Profil nicht konfiguriert. Sie ist in Beispielen enthalten, die vom Decoder ausgegeben werden.<br /> | 
| WM_SampleExtensionGUID_SampleProtectionSalt | Die Daten werden nach Beispiel verschlüsselt. Dieser Beispielerweiterungstyp wird für Inhalte verwendet, die aus einem Nicht-ASF-Dateiformat und einem anderen Rechteschutzschema als Windows Medien-DRM importiert werden. Beim Importieren geschützter Inhalte muss jedes Beispiel einen eindeutigen Salt enthalten. In der Regel ist dieser Wert ein monoton steigender Indikator.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 





