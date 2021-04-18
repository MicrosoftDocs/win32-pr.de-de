---
description: Die folgenden Funktionen werden mit Clipping verwendet.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Clipping-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf202d5ba102095c6bfddb3c3928cab1e55a230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978768"
---
# <a name="clipping-functions"></a>Clipping-Funktionen

Die folgenden Funktionen werden mit Clipping verwendet.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Excludebug**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Erstellt einen neuen Clippingbereich, der aus dem vorhandenen Clippingbereich abzüglich des angegebenen Rechtecks besteht.                                                                                |
| [**Extselectcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Kombiniert den angegebenen Bereich mit dem aktuellen Clippingbereich unter Verwendung des angegebenen Modus.                                                                                                  |
| [**Getclipbox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Ruft die Dimensionen des Zieh baren Zieh Rechtecks ab, das um den aktuell sichtbaren Bereich auf dem Gerät gezeichnet werden kann.                                                              |
| [**Getcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Ruft ein Handle ab, das den aktuellen, von der Anwendung definierten Clippingbereich für den angegebenen Gerätekontext identifiziert.                                                                          |
| [**Getmetargn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Ruft die aktuelle metaregion für den angegebenen Gerätekontext ab.                                                                                                                        |
| [**Getrandomrgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Kopiert den systemclippingbereich eines angegebenen Geräte Kontexts in eine bestimmte Region.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Erstellt einen neuen Clippingbereich aus der Schnittmenge des aktuellen Clippingbereichs und des angegebenen Rechtecks.                                                                           |
| [**Offsetcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Verschiebt den Ausschneide Bereich eines Geräte Kontexts um die angegebenen Offsets.                                                                                                                   |
| [**Ptvisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Bestimmt, ob sich der angegebene Punkt innerhalb des Ausschneide Bereichs eines Geräte Kontexts befindet.                                                                                                 |
| [**Rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Bestimmt, ob ein Teil des angegebenen Rechtecks innerhalb des Clippingbereichs eines Geräte Kontexts liegt.                                                                               |
| [**Selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Wählt den aktuellen Pfad als Clippingbereich für einen Gerätekontext aus, wobei die neue Region mit einem beliebigen vorhandenen Clippingbereich unter Verwendung des angegebenen Modus kombiniert wird.                               |
| [**Selectcliprgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Wählt eine Region als aktuellen Clippingbereich für den angegebenen Gerätekontext aus.                                                                                                         |
| [**Setmetargn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Schneidet den aktuellen Clippingbereich für den angegebenen Gerätekontext mit der aktuellen metaregion ab und speichert die kombinierte Region als neue metaregion für den angegebenen Gerätekontext. |



 

 

 



