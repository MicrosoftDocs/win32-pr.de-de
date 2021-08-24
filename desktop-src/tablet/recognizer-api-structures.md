---
description: In diesem Abschnitt werden die Recognizer-Strukturen beschrieben.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Erkennen von Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b04dbee480993a50c3ed3b8847e6595df76347f36a179d1205d8b49807c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596590"
---
# <a name="recognizer-structures"></a>Erkennen von Strukturen

In diesem Abschnitt werden die Recognizer-Strukturen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Struktur                                                    | Beschreibung                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ZEICHENBEREICH**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Gibt einen Bereich von Unicode-Punkten (Zeichen) an.<br/>                                                                                                  |
| [**LATTICE-METRIKEN \_**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Beschreibt die Baseline und die Höhe der Mittleren.<br/>                                                                                                     |
| [**LINE \_ SEGMENT**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Beschreibt die Start- und Endpunkte eines Linienerkennungssegments, z. B. die Baseline oder die Mittellinie.<br/>                                                 |
| [**\_PAKETBESCHREIBUNG**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Beschreibt den Inhalt des Pakets für einen bestimmten Tablet-Kontext.<br/>                                                                               |
| [**\_PACKET-EIGENSCHAFT**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Beschreibt eine Paketeigenschaft, die vom Tablettreiber gemeldet wird.<br/>                                                                                 |
| [**\_EIGENSCHAFTENMETRIKEN**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Definiert den Bereich und die Auflösung einer Paketeigenschaft.<br/>                                                                                             |
| [**RECO \_ ATTRS**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Ruft die Attribute einer Erkannten ab oder gibt an, welche Attribute beim Suchen nach einer installierten Recognizer verwendet werden.<br/>                         |
| [**LEITFADEN \_ ZU RECO**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Definiert die Begrenzungen der Ink-Datei für die Recognizer-Datei.<br/>                                                                                               |
| [**\_RECO-LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Dient als Einstiegspunkt in ein Lattice.<br/>                                                                                                          |
| [**\_RECO-LATTICE-SPALTE \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Stellt eine Spalte im Lattice dar.<br/>                                                                                                                |
| [**RECO \_ LATTICE-ELEMENT \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Entspricht in der Regel einem Wort oder einem ostasiatischen Zeichen. Ein Element kann jedoch auch einer Geste, einer Form oder einem anderen Code entsprechen.<br/> |
| [**\_RECO-LATTICE-EIGENSCHAFTEN \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Enthält ein Array von Zeigern auf Eigenschaftenstrukturen.<br/>                                                                                              |
| [**\_RECO-LATTICE-EIGENSCHAFT \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Enthält eine Eigenschaft, die im Lattice verwendet wird.<br/>                                                                                                           |
| [**RECO \_ RANGE**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifiziert einen Zeichenbereich in der Ergebniszeichenfolge.<br/>                                                                                             |
| [**\_STRICHBEREICH**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Gibt einen Bereich von Strichen im [**InkDisp-Objekt**](inkdisp-class.md) an.<br/>                                                                       |



 

 

 




