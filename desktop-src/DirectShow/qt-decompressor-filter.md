---
description: QT-Dekomprimiererfilter
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT-Dekomprimiererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f28058a1c729c9d42b20651a86ba31b4d98c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467967"
---
# <a name="qt-decompressor-filter"></a>QT-Dekomprimiererfilter

Diese Komponente wurde aus Windows Vista und späteren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

Der QT-Dekomprimiererfilter dekomprimiert Apple® QuickTime® 2.0-Video. Dieses Format wird in der Regel in älteren QuickTime-Dateien verwendet.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Eingabepinmedientypen | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| CLSID_QTDec | | CLSID-| der Eigenschaftenseite Keine Eigenschaftenseite. | | Ausführbare | quartz.dll | | <a href="merit.md">|</a> MERIT_NORMAL | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




