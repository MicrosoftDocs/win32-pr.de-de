---
description: Die folgenden Funktionen werden mit Clipping verwendet.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Clippingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e3ec1c57713a87e5367ed28427caaab663e0bcd1abfe83c4040e04a7e6d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115330"
---
# <a name="clipping-functions"></a>Clippingfunktionen

Die folgenden Funktionen werden mit Clipping verwendet.



| Funktion                                       | Beschreibung                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Erstellt einen neuen Ausschneidebereich, der aus dem vorhandenen Ausschneidebereich abzüglich des angegebenen Rechtecks besteht.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Kombiniert den angegebenen Bereich mit dem aktuellen Ausschneidebereich unter Verwendung des angegebenen Modus.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Ruft die Abmessungen des engsten umgebundenen Rechtecks ab, das um den aktuellen sichtbaren Bereich auf dem Gerät gezeichnet werden kann.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Ruft ein Handle ab, das den aktuellen anwendungsdefinierten Ausschneidebereich für den angegebenen Gerätekontext identifiziert.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Ruft den aktuellen Metabereich für den angegebenen Gerätekontext ab.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Kopiert den Systemausschneidebereich eines angegebenen Gerätekontexts in eine bestimmte Region.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Erstellt einen neuen Ausschneidebereich aus der Schnittmenge des aktuellen Ausschneidebereichs und des angegebenen Rechtecks.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Verschiebt den Ausschneidebereich eines Gerätekontexts um die angegebenen Offsets.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Bestimmt, ob sich der angegebene Punkt innerhalb des Ausschneidebereichs eines Gerätekontexts befindet.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Bestimmt, ob ein Teil des angegebenen Rechtecks innerhalb des Ausschneidebereichs eines Gerätekontexts liegt.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Wählt den aktuellen Pfad als Ausschneidebereich für einen Gerätekontext aus und kombiniert die neue Region mit einem vorhandenen Ausschneidebereich unter Verwendung des angegebenen Modus.                               |
| [**Wählen SieClipRgn aus.**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Wählt einen Bereich als aktuellen Ausschneidebereich für den angegebenen Gerätekontext aus.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Überschneidet den aktuellen Clippingbereich für den angegebenen Gerätekontext mit der aktuellen Metaregion und speichert den kombinierten Bereich als neuen Metaregion für den angegebenen Gerätekontext. |



 

 

 



