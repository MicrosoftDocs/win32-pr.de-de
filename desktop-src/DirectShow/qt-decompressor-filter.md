---
description: QT-Dekomprimiererfilter
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT-Dekomprimiererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983648"
---
# <a name="qt-decompressor-filter"></a>QT-Dekomprimiererfilter

Diese Komponente wurde aus Windows Vista und späteren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

Der QT-Dekomprimiererfilter dekomprimiert Apple® QuickTime® 2.0-Video. Dieses Format wird in der Regel in älteren QuickTime-Dateien verwendet.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Eingabepinmedientypen | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| Eingabe-Pin-Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Medientypen des Ausgabepins | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | 
| Ausgabe-Pin-Schnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern von CLSID | CLSID_QTDec | 
| CLSID der Eigenschaftenseite | Keine Eigenschaftenseite. | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




