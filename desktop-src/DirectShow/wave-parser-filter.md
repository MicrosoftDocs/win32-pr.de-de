---
description: WAVE-Parserfilter
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: WAVE-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91508500b02743f7cac8b4ed5cff718d12e3b03
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987853"
---
# <a name="wave-parser-filter"></a>WAVE-Parserfilter

Der WAVE-Parserfilter analysiert Audiodaten im WAV-Format aus WAV-, AU- oder AIF-Dateien. Der Upstreamfilter muss der [Filter "Asynchrone](file-source--async--filter.md) Dateiquelle", ["URL-Dateiquelle"](file-source--url--filter.md) oder ein kompatibler asynchroner Quellfilter eines Drittanbieters sein, der WAV-Audiodaten enthält. Der Ausgabestream sind Audiodaten, die Sie direkt mit einem Audiorenderingfilter oder einem intervening audio transform filter verbinden können.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a> | 
| Eingabepin-Medientypen | Haupttyp: MEDIATYPE_StreamThe folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | Haupttyp: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM oder anderer Komprimierungstyp. (Siehe <a href="audio-subtypes.md"><strong>Audiountertypen</strong></a>.)<br /> Formattyp: FORMAT_WaveFormatEx<br /> | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| Filtern der CLSID | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | 
| Eigenschaftenseite CLSID | Keine Eigenschaftenseite. | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Bemerkungen

Dieser Filter unterstützt die folgenden Dateitypen:

-   WAVE (.wav)
-   AIFF und AIFF-C (.aif)
-   AU (.au)

Für das Audioformat gelten jedoch die folgenden Einschränkungen:

-   Die Audiodaten müssen ein lineares 8-Bit- oder 16-Bit-PCM sein.
-   Bei AIFF-C-Dateien muss die Audiodatei in Big-Endian-Byte-Reihenfolge (Komprimierungstyp "NONE") dekomprimiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




