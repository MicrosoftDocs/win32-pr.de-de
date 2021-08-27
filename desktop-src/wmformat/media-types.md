---
title: Medientypen für Windows Media Format SDK
description: Erfahren Sie mehr über Medientypen, die vom SDK für Windows Medienformat verwendet werden können. Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen sind.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Medienformat-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Medientypen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84974391a7e044367fd298598181d43447cfac4bec1829b9e5ddb0b90ae27ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027488"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Medientypen für Windows Media Format SDK

Medientypen identifizieren die verschiedenen Medientypen, die vom Windows Media Format SDK verwendet werden können. Alle Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen wurden. Die GUID-Werte, die durch die in diesem [](media-type-identifiers.md) Abschnitt aufgeführten Konstanten dargestellt werden, sind im Abschnitt Medientypbezeichner dieser Referenz aufgeführt.

In der folgenden Tabelle sind die wichtigsten Medientypen aufgeführt. Diese Konstanten definieren die hohe Klassifizierung digitaler Medien, die vom Windows Media Format SDK unterstützt werden.



| Haupttyp                | Beschreibung                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| WMMEDIATYPE-Video \_        | Ein Videostream.                                                                                         |
| WMMEDIATYPE-Audio \_        | Ein Audiostream.                                                                                        |
| WMMEDIATYPE-Skript \_       | Ein Skriptstream.                                                                                        |
| WMMEDIATYPE \_ FileTransfer | Ein Stream, der Datendateien enthält. Webstreams, die aus HTML-Dateien bestehen, haben ebenfalls diesen Haupttyp. |
| WMMEDIATYPE-Image \_        | Ein JPEG-Bildstream für eine dargestellte Audiodatei (wie in einer Bildschirmpräsentation).                                 |
| WMMEDIATYPE-Text \_         | Ein Textstream.                                                                                          |



 

Zusätzlich zu den explizit unterstützten Hauptmedientypen können Sie eigene beliebige Datentypen erstellen. Für benutzerdefinierte beliebige Datentypen müssen Sie sicherstellen, dass die von Ihnen verwendete GUID nicht mit einem vorhandenen Haupttyp übereinstimmen.

Ein Medienstream verfügt häufig zusätzlich zu seinem Haupttyp über einen Untertyp. In den folgenden Abschnitten werden die unterstützten Untertypen aufgeführt.



| `Section`                                                        | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Unkomprimierte Medienuntertypen](uncompressed-media-subtypes.md) | Beschreibt die Untertypen, die für unkomprimierte Medien verfügbar sind. Dies sind die Typen, die in der Regel eingabe- oder ausgabemedien zugeordnet sind.              |
| [Komprimierte Medienuntertypen](compressed-media-subtypes.md)     | Beschreibt die Untertypen, die für komprimierte Medien verfügbar sind. Dies sind die Typen, die in der Regel Medien in einem Stream innerhalb einer ASF-Datei zugeordnet sind. |
| [Videoeingabeformate](video-input-formats.md)                 | Listet die Videoformate auf, die als Eingaben für den Windows Media Video 9-Codec akzeptiert werden.                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medientypbezeichner**](media-type-identifiers.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




