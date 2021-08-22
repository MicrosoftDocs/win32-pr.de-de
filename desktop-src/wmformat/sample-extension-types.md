---
title: Stichprobenerweiterungstypen
description: Stichprobenerweiterungstypen
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, Beispielerweiterungen
- Advanced Systems Format (ASF), Beispielerweiterungen
- ASF (Advanced Systems Format), Beispielerweiterungen
- Windows Medienformat-SDK, Dateneinheitserweiterungen
- Advanced Systems Format (ASF), Dateneinheitserweiterungen
- ASF (Advanced Systems Format), Dateneinheitserweiterungen
- Windows Medienformat-SDK, Puffereigenschaften
- Advanced Systems Format (ASF), Puffereigenschaften
- ASF (Advanced Systems Format), Puffereigenschaften
- Beispielerweiterungen,Typen
- Dateneinheitserweiterungen,Typen
- Puffereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94161486fee7a31419f2e7fb9af2ed7fc968f00e8b43b81c58254547ec2f74e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119345390"
---
# <a name="sample-extension-types"></a>Stichprobenerweiterungstypen

Beispielerweiterungen, die auch als Dateneinheitserweiterungen (DATA Unit Extensions, DUEs) oder Puffereigenschaften bezeichnet werden, sind Datenelemente, die an die Medienbeispiele im Datenabschnitt der ASF-Datei angefügt werden. Verschiedene Arten von Beispielerweiterungen werden im Windows Media Format SDK definiert. Sie können auch eigene Erweiterungstypen erstellen.

Um Beispielerweiterungen zu verwenden, müssen Sie den Erweiterungstyp in den Datenstromkonfigurationsdaten des Profils identifizieren. Rufen Sie [**die IWMStreamConfig2::AddDataUnitExtension-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) auf, um einen Stream zum Akzeptieren von Beispielen mit erweiterten Daten zu konfigurieren.

Einzelne Beispielerweiterungen müssen den Eingabebeispielen durch Aufrufen der [**INSSBuffer3::SetProperty-Methode hinzugefügt**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) werden. Beim Lesen von Beispielen können Sie die [**INSSBuffer3::GetProperty-Methode**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) aufrufen, um die Erweiterungsdaten abzurufen. Sie können auch die Methoden der [**INSSBuffer4-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) verwenden, um die an ein Beispiel angefügten Dateneinheitserweiterungen zu aufzählen.

In der folgenden Tabelle sind die vordefinierten Bezeichner der Dateneinheitserweiterung aufgeführt, und es werden die Daten beschrieben, die den Beispielen für die einzelnen Dateien angefügt werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispielerweiterungs-GUID</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>Die Daten geben an, ob das Beispiel ein <a href="wmformat-glossary.md"><em>Cleanpoint ist.</em></a> Der Wert 0 (null) gibt an, dass das Beispiel kein Cleanpoint ist. Ein Wert, der nicht 0 (null) ist, gibt an, dass es sich um einen Cleanpoint handelt. Dieser Beispieltyp der Dateneinheitserweiterung (DUE) wird verwendet, um Cleanpoints beim Schreiben von vorkomprimierten Medienstreams zu verfolgen, die mit Codecs von Drittanbietern codiert wurden.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>Die Daten sind <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>eine</strong></a> WMT_TIMECODE_EXTENSION_DATA, die dem Beispiel zugeordnete SMPTE-Zeitcodedaten enthält. Die Größe für dieses DUE-WM_SampleExtension_Timecode_Size beträgt 14 Bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Diese Art von Beispielerweiterung wird für Dateistreams verwendet. Die Daten in einem Dateistreambeispiel sind ein Teil einer Datendatei. Die Daten in der Beispielerweiterung geben den Namen der Datei an, aus der der Inhalt des Beispiels entnommen wurde. Der Dateiname ist eine Breitzeichenfolge, die den Dateinamen im Format name.extension ohne Pfadinformationen enthält.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>Die Daten identifizieren den Inhaltstyp, den das Beispiel enthält. Diese Art von Beispielerweiterung wird mit Interlacing-Videostreams verwendet. Alle Interlacinginhalte verwenden das WM_CT_INTERLACED-Flag, das durch ein bitweises <strong>OR</strong> kombiniert wird, entweder WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST oder WM_CT_REPEAT_FIRST_FIELD.<br/> Die Feld reihenfolge wird im Codierungsprozess nicht verwendet, wird jedoch mit den komprimierten Stichproben beibehalten, sodass sie an die Renderinghardware übergeben werden kann. Die Wiedergabe von Interlacinginhalten mit der falschen Feld reihenfolge führt zu Artefakten wie Bewegungs-Jitter im Video.<br/> Die Größe dieses DUE-WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>Die Daten geben das Pixel-Seitenverhältnis des Inhalts im Beispiel an. Dies gilt nur für Videos. Dieser Erweiterungstyp wird verwendet, um das Seitenverhältnis von nicht quadratischen Pixeln zu identifizieren. Weitere Informationen finden Sie unter <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.<br/> Seitenverhältniswerte werden als Wort gespeichert, dessen niedriges Byte der X-Aspekt und dessen hohes Byte der Y-Aspekt ist. Beispielsweise wird 16:9 als 0x0910.<br/> Die Größe für dieses DUE-WM_SampleExtension_PixelAspectRatio_Size beträgt 2 Byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>Die Daten geben die Dauer des im Pufferobjekt enthaltenen Beispiels in Millisekunden an. Wenn bei der Wiedergabe dieses DUE-Werts festgelegt ist, wird es vom Readerobjekt verwendet, um den vorhandenen Wert für die Beispieldauer zu überschreiben. Dieses DUE wird automatisch von den SDK-Laufzeitkomponenten für Videostreams mit Bitraten von 100 KBit/s oder höher festgelegt, wobei der Mehraufwand der DUE-Informationen nicht signifikant ist. Sie ist nicht für Streams mit Bitraten unter 100 KBit/s festgelegt. Anwendungen sollten dies DUE nicht manuell festlegen, da der Writer (bei Datenströmen mit hoher Bitrate) den Wert mit seinen eigenen Daten überschreibt.<br/> Die Größe für dieses DUE-WM_SampleExtension_SampleDuration_Size beträgt 2 Bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>Die Daten geben den Typ des im I420-Videoformat verwendeten Subsamplingtyps an. Der Wert dieser Erweiterung wird auf einen der folgenden Werte festgelegt:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Diese Dateneinheitserweiterung ist im Profil nicht konfiguriert. Sie ist in der Beispielausgabe des Decoders enthalten.<br/> Die Größe dieses DUE-WM_SampleExtension_ChromaLocation_Size beträgt immer 1 Byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>Die Daten enthalten Informationen zum Farbraum, der für den aktuellen Videoframe verwendet wird. Der Wert dieser Erweiterung ist <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>eine</strong></a> WMT_COLORSPACEINFO_EXTENSION_DATA Struktur.<br/> Diese Dateneinheitserweiterung ist im Profil nicht konfiguriert. Sie ist in der Beispielausgabe des Decoders enthalten.<br/> Die Größe dieses DUE-WM_SampleExtension_ColorSpaceInfo_Size 3 Byte.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>Die Daten sind benutzerdefinierte Benutzerdaten. Die ersten vier Bytes der Daten enthalten die Größe der benutzerdefinierten Daten.<br/> Das nächste Byte enthält den Typ der Benutzerdaten, die in der Beispielerweiterung bereitgestellt werden. Die folgenden Typen werden unterstützt:<br/>
<ul>
<li>0x1F: Benutzerdaten auf Sequenzebene</li>
<li>0x1E: Benutzerdaten auf Einstiegspunktebene</li>
<li>0x1D: Benutzerdaten auf Frameebene</li>
<li>0x1C: Benutzerdaten auf Feldebene</li>
<li>0x1B: Sliceebenenbenutzerdaten</li>
</ul>
Das sechste und nachfolgende Bytes enthalten die Benutzerdaten. Es gibt so viele Byte von Benutzerdaten, wie durch die Zahl in den ersten vier Bytes angegeben.<br/> Diese Dateneinheitserweiterung ist im Profil nicht konfiguriert. Sie ist in Beispielen enthalten, die vom Decoder ausgegeben werden.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>Die Daten werden per Beispiel verschlüsselt. Dieser Beispielerweiterungstyp wird für Inhalte verwendet, die aus einem Nicht-ASF-Dateiformat und einem anderen Rights Protection-Schema als Windows Media DRM importiert werden. Beim Importieren geschützter Inhalte muss jedes Beispiel ein eindeutiges Salt enthalten. In der Regel ist dieser Wert ein monoton steigender Zähler.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 





