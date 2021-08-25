---
description: Die folgenden Funktionen beziehen sich auf Medientypobjekte.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Hilfsfunktionen für Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b488eb706338926aaffd3c3c4e13a5da4d1d004bd21dbbd1f5871c6d4818dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827360"
---
# <a name="media-type-helper-functions"></a>Hilfsfunktionen für Medientypen

Die folgenden Funktionen beziehen sich auf Medientypobjekte.



| Funktion                                                                     | Beschreibung                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Berechnet die Bildfrequenz aus der durchschnittlichen Dauer eines Videoframes. |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Ruft die Bildgröße für ein nicht komprimiertes Videoformat ab.            |
| [**MFCompareFullToPartialMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | Vergleicht einen vollständigen Medientyp mit einem partiellen Medientyp.                   |
| [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | Erstellt einen leeren Medientyp.                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Konvertiert eine Videobildrate in eine Framedauer.                    |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Ruft den minimalen Oberflächenschritt für ein Videoformat ab.              |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Fragt ab, ob ein FOURCC-Code oder **ein D3DFORMAT-Wert** ein YUV-Format ist. |
| [**MFValidateMediaTypeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | Überprüft die Größe eines Puffers für einen Videoformatblock.              |
| [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | Erstellt einen Medientyp, der einen anderen Medientyp umschließt.                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypkonvertierungen](media-type-conversions.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



