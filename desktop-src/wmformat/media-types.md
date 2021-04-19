---
title: Medientypen für das Windows Media-Format-SDK
description: Erfahren Sie mehr über Medientypen, die vom SDK für den Windows Media-Format verwendet werden können. Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen werden.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media-Format-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Medientypen, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106370975"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Medientypen für das Windows Media-Format-SDK

Mit Medientypen werden die unterschiedlichen Medientypen identifiziert, die vom SDK für den Windows Media-Format verwendet werden können. Alle Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen wurden. Die GUID-Werte, die von den in diesem Abschnitt aufgeführten Konstanten dargestellt werden, sind im Abschnitt [Medientyp](media-type-identifiers.md) -IDs dieses Verweises aufgeführt.

In der folgenden Tabelle sind die wichtigsten Medientypen aufgeführt. Diese Konstanten definieren die allgemeine Klassifizierung digitaler Medien, die vom SDK für den Windows Media-Format unterstützt werden.



| Haupttyp                | BESCHREIBUNG                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Wmmediatype- \_ Video        | Ein Videostream.                                                                                         |
| Wmmediatype \_ -Audiodatei        | Ein Audiodatenstrom.                                                                                        |
| Wmmediatype- \_ Skript       | Ein Skript Datenstrom.                                                                                        |
| Wmmediatype- \_ Filetransfer | Ein Datenstrom, der Datendateien enthält. Webstreams, die aus HTML-Dateien bestehen, haben ebenfalls diesen Haupttyp. |
| Wmmediatype- \_ Image        | Ein JPEG-Bildstream für eine dargestellte Audiodatei (wie in einer Folien Anzeige).                                 |
| Wmmediatype- \_ Text         | Ein Textstream.                                                                                          |



 

Zusätzlich zu den explizit unterstützten Hauptmedien Typen können Sie auch eigene beliebige Datentypen erstellen. Für benutzerdefinierte beliebige Datentypen müssen Sie sicherstellen, dass die von Ihnen verwendete GUID nicht mit einem vorhandenen Haupttyp identisch ist.

Ein Mediendaten Strom weist neben seinem Haupttyp häufig einen Untertyp auf. In den folgenden Abschnitten sind die Untertypen aufgeführt.



| `Section`                                                        | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Nicht komprimierte Medien Untertypen](uncompressed-media-subtypes.md) | Beschreibt die Untertypen, die für nicht komprimierte Medien verfügbar sind. Dabei handelt es sich um Typen, die normalerweise mit Eingabe-oder Ausgabemedien verknüpft sind              |
| [Komprimierte Medien Untertypen](compressed-media-subtypes.md)     | Beschreibt die Untertypen, die für komprimierte Medien verfügbar sind. Dabei handelt es sich um die Typen, die normalerweise Medien in einem Stream innerhalb einer ASF-Datei zugeordnet sind. |
| [Video Eingabeformate](video-input-formats.md)                 | Listet die Videoformate auf, die als Eingaben für den Windows Media Video 9-Codec akzeptiert werden.                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medientyp-IDs**](media-type-identifiers.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 




