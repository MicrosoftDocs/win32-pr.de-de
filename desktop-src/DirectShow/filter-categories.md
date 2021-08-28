---
description: In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filterkategorien aufgeführt.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filterkategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476326"
---
# <a name="filter-categories"></a>Filterkategorien

In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filterkategorien aufgeführt.

-   [DirectShow-Filterkategorien](#directshow-filter-categories)
-   [Andere Filterkategorien](#other-filter-categories)
-   [DirectShow Filter Meta-Category](#directshow-filter-meta-category)
-   [DMO Kategorien](#dmo-categories)
-   [Zugehörige Themen](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow-Filterkategorien

Die hier aufgeführten Kategorien werden vom Filter [mapper aufgelistet.](filter-mapper.md) Standardmäßig ignoriert der Filter-Mapper jedoch Kategorien mit den Vorteilen VON NICHT VERWENDEN \_ \_ oder \_ weniger. Weitere Informationen finden Sie unter [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Alle hier aufgeführten Kategorien können auch mit dem [Systemgeräte-Enumerator aufgelistet werden.](system-device-enumerator.md)

Die folgenden Kategorien werden in Uuids.h deklariert. Schließen Sie die Headerdatei Dshow.h ein.




| Anzeigename | CLSID | Verdienst | 
|---------------|-------|-------|
| Audioaufnahmequellen | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Audiowiedergaben | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Audiorenderer | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Gerätesteuerungsfilter | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow-Filter | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Externe Renderer | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Renderer von Renderern | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Videoaufnahmequellen | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Videobeendungen | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM-Datenstrom-Dekomprimierungsgeräte | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />Diese Kategorie enthält Hardware-DVD-Decoder.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM-Streamingerfassungsgeräte | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming Crossbar Devices | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM-Streamingrenderinggeräte | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming Tee/Splitter Devices | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming TV Audio Devices | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM Streaming TV Tuner Devices | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM-Streaming-VBI-Codecs | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

Die folgenden Kategorien werden in der Headerdatei Ks.h deklariert.



| Anzeigename                          | CLSID                                   | Verdienst                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| WDM-Streamingkommunikationstransformationen | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **NICHT \_ \_ VERWENDEN \_** |
| WDM-Streamingdatentransformationen          | **KSCATEGORY \_ DATATRANSFORM**           | **NICHT \_ \_ VERWENDEN \_** |
| Transformationen der WDM-Streamingschnittstelle     | **\_KSCATEGORY-SCHNITTSTELLETRANSFORM**      | **NICHT \_ \_ VERWENDEN \_** |
| WDM-Streaming Mixer Geräte            | **KSCATEGORY \_ MIXER**                   | **NICHT \_ \_ VERWENDEN \_** |



 

Die folgenden Kategorien werden in der Headerdatei Bdamedia.h deklariert. Schließen Sie die folgenden Headerdateien ein: ks.h, ksmedia.h und bdamedia.h.



| Anzeigename                       | CLSID                                       | Verdienst                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA-Netzwerkanbieter               | **KSCATEGORY \_ \_ BDA-NETZWERKANBIETER \_**      | **MERIT \_ NORMAL**       |
| BDA-Empfängerkomponenten             | **KSCATEGORY \_ \_ BDA-EMPFÄNGERKOMPONENTE \_**    | **NICHT \_ \_ VERWENDEN \_** |
| BDA-Renderingfilter               | **\_KSCATEGORY-IP-SENKE \_**                    | **NICHT \_ \_ VERWENDEN \_** |
| BDA-Quellfilter                  | **KSCATEGORY \_ \_ BDA-NETZWERK-TUNER \_**         | **NICHT \_ \_ VERWENDEN \_** |
| BDA-Transportinformationsrenderer | **KSCATEGORY \_ \_ BDA-TRANSPORTINFORMATIONEN \_** | **MERIT \_ NORMAL**       |



 

> [!Note]  
> Decoder werden unter der Kategorie "DirectShow Filters" (CLSID \_ LegacyAmFilterCategory) registriert.

 

## <a name="other-filter-categories"></a>Andere Filterkategorien

Die hier aufgeführten Kategorien können mit dem Systemgeräte-Enumerator aufgelistet werden, sind für die Filterzuordnung jedoch nicht sichtbar und werden nicht von [Intelligent Verbinden.](intelligent-connect.md)

Die folgenden Kategorien werden in der Headerdatei Qedit.h deklariert.



| Anzeigename            | CLID                             | Verdienst                   |
|--------------------------|----------------------------------|-------------------------|
| Videoeffekte (1 Eingabe)  | **CLSID \_ VideoEffects1Category** | **NICHT \_ \_ VERWENDEN \_** |
| Videoeffekte (2 Eingaben) | **CLSID \_ VideoEffects2Category** | **NICHT \_ \_ VERWENDEN \_** |



 

Diese Kategorien enthalten Videoeffekte und Übergänge für [DirectShow Editing Services:](directshow-editing-services.md)

-   "Videoeffekte (1 Eingabe)" enthält Videoeffekte.
-   "Videoeffekte (2 Eingabe)" enthält Videoübergänge.

Weitere Informationen finden Sie unter [Aufzählen von Effekten und Übergängen.](enumerating-effects-and-transitions.md)

Die folgenden Kategorien werden in der Headerdatei Uuids.h deklariert. Schließen Sie die Headerdatei Dshow.h ein.



| Anzeigename       | CLID                                | Verdienst                   |
|---------------------|-------------------------------------|-------------------------|
| EncAPI-Encoder     | **CLSID \_ MediaEncoderCategory**     | **NICHT \_ \_ VERWENDEN \_** |
| EncAPI-Multiplexer | **CLSID \_ MediaMultiplexerCategory** | **NICHT \_ \_ VERWENDEN \_** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow-Filter Meta-Category



| Anzeigename                 | CLSID                            | Verdienst          |
|-------------------------------|----------------------------------|----------------|
| ActiveMovie-Filterkategorien | **CLSID \_ ActiveMovieCategories** | Nicht zutreffend |



 

Diese Metakategorie enthält eine Liste von Filterkategorien. Wenn in dieser Liste keine Filterkategorie angezeigt wird, ignoriert der [Filter mapper](filter-mapper.md) die Kategorie, was bedeutet, dass der Filter für [Intelligent](intelligent-connect.md)Verbinden.

Rufen Sie zum Auflisten der Liste der Filterkategorien [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit dem Wert CLSID \_ ActiveMovieCategories auf. Die von dieser Methode zurückgegebenen Moniker unterstützen die folgenden Eigenschaften.



| Eigenschaftenname  | BESCHREIBUNG                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| "FriendlyName" | Kategoriename (VT \_ BSTR).                                                              |
| "Besendung"        | Kategorieknind (VT \_ I4). Wenn diese Eigenschaft nicht vorhanden ist, behandeln Sie **als NICHT \_ VERWENDEN. \_ \_** |
| "CLSID"        | Kategorie-CLSID (VT \_ BSTR).                                                             |



 

Um dieser Liste eine neue Filterkategorie hinzuzufügen, rufen Sie [**IFilterMapper2::CreateCategory auf.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory)

## <a name="dmo-categories"></a>DMO Kategorien

DirectX Media Objects (DMOs) verwenden einen anderen Enumerationsmechanismus als DirectShow-Filter. Weitere Informationen finden Sie unter [Registrieren eines DMO](registering-a-dmo.md). Sie können jedoch den Systemgeräte-Enumerator verwenden, um DMO aufzählen. Die Moniker werden an den DMO [Wrapperfilter](dmo-wrapper-filter.md) gebunden und initialisieren den Filter automatisch mit dem DMO.

Darüber hinaus werden einige der DMO Filterkategorien für intelligente Verbindungen DirectShow-Filterkategorien zugeordnet:



| DMO Kategorie                    | DirectShow-Entsprechung              |
|---------------------------------|------------------------------------|
| **\_DMOCATEGORY-AUDIOENCODER \_** | **CLSID \_ AudioCompressorCategory** |
| **\_DMOCATEGORY-AUDIODECODER \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **\_DMOCATEGORY-VIDEOENCODER \_** | **CLSID \_ VideoCompressorCategory** |
| **\_DMOCATEGORY-VIDEODECODER \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Beachten Sie, dass die Kategorien "Videoeffekt" und "Audioeffekt" keinen DirectShow-Kategorien zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Aufzählen von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Intelligente Verbinden](intelligent-connect.md)
</dt> <dt>

[Layout der Registrierungsschlüssel](layout-of-the-registry-keys.md)
</dt> <dt>

[Verwenden der Filterzuordnung](using-the-filter-mapper.md)
</dt> <dt>

[Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




