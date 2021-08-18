---
description: Eine erweiterte Metadatei ist ein Array von Datensätzen.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Erweiterte Metadateidatensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506ca77dda1bd90fc04b692dbbd98bc06f4da44c5fc6f8edb0fd17cbd3e94c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038018"
---
# <a name="enhanced-metafile-records"></a>Erweiterte Metadateidatensätze

Eine erweiterte Metadatei ist ein Array von Datensätzen. Ein Metadateidatensatz ist eine [**ENHMETARECORD-Struktur variabler**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) Länge. Am Anfang jedes erweiterten Metadateidateneintrags befindet sich eine [**EMR-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-emr) die zwei Member enthält. Der erste Member, iType, identifiziert den Datensatztyp, d. h. die GDI-Funktion, deren Parameter im Datensatz enthalten sind. Da die Strukturen eine variable Länge haben, enthält der andere Member nSize die Größe des Datensatzes. Unmittelbar nach dem nSize-Member befinden sich die verbleibenden Parameter der GDI-Funktion(sofern verfügbar). Der Rest der Struktur enthält zusätzliche Daten, die vom Datensatztyp abhängig sind.

Der erste Datensatz in einer erweiterten Metadatei ist immer die [**ENHMETAHEADER-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) bei der es sich um den Enhanced-Metafile-Header handelt. Der -Header gibt die folgenden Informationen an:

-   Größe der Metadatei in Bytes
-   Abmessungen des Bilderrahmens in Geräteeinheiten
-   Abmessungen des Bilderrahmens in Einheiten von 0,01 Millimeter
-   Anzahl der Datensätze in der Metadatei
-   Offset zu einer optionalen Textbeschreibung
-   Größe der optionalen Palette
-   Auflösung des ursprünglichen Geräts in Pixel
-   Auflösung des ursprünglichen Geräts in Millimeter

Eine optionale Textbeschreibung kann dem Headerdatensatz folgen. Die Textbeschreibung beschreibt das Bild und den Namen des Autors. Die optionale Palette gibt die Farben an, die zum Erstellen der erweiterten Metadatei verwendet werden. Die verbleibenden Datensätze identifizieren die GDI-Funktionen, die zum Erstellen des Bilds verwendet werden. Die folgende hexadezimale Ausgabe entspricht einem Datensatz, der für einen Aufruf der [**SetMapMode-Funktion generiert**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) wurde.


```C++
00000011 0000000C 00000004 
```



Der Wert 0x00000011 den Datensatztyp an (entspricht der IN der Datei Wingdi.h definierten EMR \_ SETMAPMODE-Konstante). Der Wert 0x0000000C gibt die Länge des Datensatzes in Bytes an. Der Wert 0x00000004 identifiziert den Zuordnungsmodus (entspricht der in der SetMapMode-Funktion definierten MM \_ LOENGLISH-Konstante). [](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)

Eine Liste der zusätzlichen Datensatztypen finden Sie unter [Metafile-Strukturen](metafile-structures.md).

 

 



