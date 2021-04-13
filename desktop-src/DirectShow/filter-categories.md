---
description: In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filter Kategorien aufgeführt.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filter Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392367"
---
# <a name="filter-categories"></a>Filter Kategorien

In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filter Kategorien aufgeführt.

-   [DirectShow-Filter Kategorien](#directshow-filter-categories)
-   [Weitere Filter Kategorien](#other-filter-categories)
-   [DirectShow-Filter-metakategorie](#directshow-filter-meta-category)
-   [DMO-Kategorien](#dmo-categories)
-   [Zugehörige Themen](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow-Filter Kategorien

Die hier aufgeführten Kategorien werden vom [Filter Mapper](filter-mapper.md)aufgelistet. In der Standardeinstellung ignoriert der Filter Mapper jedoch Kategorien, bei denen Vorzüge von Vorteilen \_ \_ nicht \_ oder weniger verwendet werden. Weitere Informationen finden Sie unter [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Alle hier aufgeführten Kategorien können auch mit dem [Enumerator für System Geräte](system-device-enumerator.md)aufgelistet werden.

Die folgenden Kategorien werden in "UUIDs. h" deklariert. Schließen Sie die Header Datei DShow. h ein.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Anzeigename</th>
<th>CLSID</th>
<th>Verdienst</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Audioerfassungs Quellen</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Audiokompressoren</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Audiorenderer</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Geräte Steuerungs Filter</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>DirectShow-Filter</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Externe Renderer</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>MIDI-Renderer</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Video Erfassungs Quellen</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Video-Kompressoren</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM-streamdekomprimierungsgeräte</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
Diese Kategorie enthält Hardware-DVD-Decoder.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM-Streaming-Erfassungsgeräte</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM-Streaming-Crossbar-Geräte</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM Streaming-renderinggeräte</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM-Streaming-Tee/Splitter-Geräte</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM Streaming TV-Audiogeräte</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM-Streaming TV-Tuner-Geräte</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM-Streaming-VBI-Codecs</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Die folgenden Kategorien werden in der Header Datei ". h" deklariert.



| Anzeigename                          | CLSID                                   | Verdienst                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| WDM-streamingkommunikationstransformationen | **kscategory \_ communicationstransform** | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| WDM-streamingdatentransformationen          | **kscategory \_ DataTransform**           | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| WDM-Streaming-Schnittstellen Transformationen     | **kscategory \_ interfacetransform**      | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| WDM-Streaming-Mischgeräte            | **kscategory- \_ Mixer**                   | **das Verdienst wird \_ \_ nicht \_ verwendet.** |



 

Die folgenden Kategorien werden in der Header Datei bdamedia. h deklariert. Fügen Sie die folgenden Header Dateien ein: "KS. h", "ksmedia. h" und "bdamedia. h".



| Anzeigename                       | CLSID                                       | Verdienst                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA-Netzwerkanbieter               | **kscategory- \_ BDA- \_ Netzwerk \_ Anbieter**      | **Verdienst \_ Normal**       |
| BDA-Empfänger Komponenten             | **kscategory- \_ BDA \_ Empfänger \_ Komponente**    | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| BDA-Rendering-Filter               | **kscategory \_ -IP- \_ Senke**                    | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| BDA-Quell Filter                  | **kscategory- \_ BDA- \_ Netzwerk- \_ Tuner**         | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| BDA-Transport Informations Renderer | **kscategory- \_ BDA- \_ Transport \_ Informationen** | **Verdienst \_ Normal**       |



 

> [!Note]  
> Decoders werden unter der Kategorie "DirectShow-Filter" (CLSID \_ legacyamfiltercategory) registriert.

 

## <a name="other-filter-categories"></a>Weitere Filter Kategorien

Die hier aufgeführten Kategorien können mit dem Enumerator für System Geräte aufgelistet werden, sind aber für die Filter Zuordnung nicht sichtbar und werden nicht von [Intelligent Connect](intelligent-connect.md)verwendet.

Die folgenden Kategorien sind in der Header Datei "qedit. h" deklariert.



| Anzeigename            | CLID                             | Verdienst                   |
|--------------------------|----------------------------------|-------------------------|
| Video Effekte (1 Eingabe)  | **CLSID- \_ VideoEffects1Category** | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| Video Effekte (2 Eingaben) | **CLSID- \_ VideoEffects2Category** | **das Verdienst wird \_ \_ nicht \_ verwendet.** |



 

Diese Kategorien enthalten Video Effekte und Übergänge für [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md):

-   "Video Effekte (1 Eingabe)" enthält Video Effekte.
-   "Video Effekte (2 Eingabe)" enthält Video Übergänge.

Weitere Informationen finden Sie unter [Enumerieren von Effekten und Übergängen](enumerating-effects-and-transitions.md).

Die folgenden Kategorien sind in der Header Datei "UUIDs. h" deklariert. Schließen Sie die Header Datei DShow. h ein.



| Anzeigename       | CLID                                | Verdienst                   |
|---------------------|-------------------------------------|-------------------------|
| Umcapi-Encoder     | **CLSID \_ mediaencodercategory**     | **das Verdienst wird \_ \_ nicht \_ verwendet.** |
| Umcapi-Multiplexer | **CLSID \_ mediamultiplexercategory** | **das Verdienst wird \_ \_ nicht \_ verwendet.** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow-Filter Meta-Category



| Anzeigename                 | CLSID                            | Verdienst          |
|-------------------------------|----------------------------------|----------------|
| ActiveMovie-Filter Kategorien | **CLSID \_ activemoviecategories** | Nicht verfügbar |



 

Diese metakategorie enthält eine Liste mit Filter Kategorien. Wenn eine Filterkategorie nicht in dieser Liste angezeigt wird, ignoriert der [Filter Mapper](filter-mapper.md) die Kategorie. Dies bedeutet, dass der Filter für eine [intelligente Verbindung](intelligent-connect.md)nicht verfügbar ist.

Um die Liste der Filter Kategorien aufzulisten, nennen Sie [**ikreatedevenum:: kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit dem Wert CLSID \_ activemoviecategories. Die von dieser Methode zurückgegebenen Moniker unterstützen die folgenden Eigenschaften.



| Eigenschaftenname  | BESCHREIBUNG                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Kategoriename (VT \_ BSTR).                                                              |
| Verdienst        | Kategorie-Verdienst (VT \_ I4). Wenn diese Eigenschaft nicht vorhanden ist, **\_ \_ \_ verwenden Sie als Verdienst nicht**. |
| CLSID        | Kategorie CLSID (VT \_ BSTR).                                                             |



 

Um dieser Liste eine neue Filterkategorie hinzuzufügen, nennen Sie [**IFilterMapper2:: | atecategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO-Kategorien

DirectX Media Objects (DMOs) verwenden einen anderen enumerationsmechanismus als DirectShow-Filter. Weitere Informationen finden Sie unter [Registrieren eines DMO](registering-a-dmo.md). Sie können jedoch den Enumerator "System Geräte" verwenden, um DMO-Kategorien aufzulisten. Die Moniker binden an den [DMO-Wrapper Filter](dmo-wrapper-filter.md) und initialisieren den Filter automatisch mit dem DMO.

Außerdem werden einige der DMO-Kategorien für die intelligente Verbindung zu den DirectShow-Filter Kategorien zugeordnet:



| DMO-Kategorie                    | DirectShow-Entsprechung              |
|---------------------------------|------------------------------------|
| **dmucategory \_ - \_ Audioencoder** | **CLSID \_ audiocompressorcategory** |
| **dmucategory \_ - \_ Audiodecoder** | **CLSID \_ legacyamfiltercategory**  |
| **dmucategory- \_ Video \_ Encoder** | **CLSID \_ videocompressorcategory** |
| **dmucategory- \_ Video \_ Decoder** | **CLSID \_ legacyamfiltercategory**  |



 

Beachten Sie, dass die Kategorien "Videoeffekt" und "Audioeffekt" keiner DirectShow-Kategorie zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Auflisten von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Intelligent Connect](intelligent-connect.md)
</dt> <dt>

[Layout der Registrierungsschlüssel](layout-of-the-registry-keys.md)
</dt> <dt>

[Verwenden des Filter Mappers](using-the-filter-mapper.md)
</dt> <dt>

[Verwenden des Enumerators für System Geräte](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




