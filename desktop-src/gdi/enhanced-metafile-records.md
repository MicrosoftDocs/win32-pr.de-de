---
description: Eine erweiterte Metadatei ist ein Array von Datensätzen.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Erweiterte Metafile-Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978617"
---
# <a name="enhanced-metafile-records"></a>Erweiterte Metafile-Datensätze

Eine erweiterte Metadatei ist ein Array von Datensätzen. Ein Metadateidatensatz ist eine " [**enhmetarecord**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) "-Struktur mit variabler Länge. Am Anfang jedes erweiterten Metadateidatensatz ist eine [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) -Struktur, die zwei Member enthält. Der erste Member, ITYPE, identifiziert den Daten Satz Typen, d. h. die GDI-Funktion, deren Parameter im Datensatz enthalten sind. Da die-Strukturen eine Variable Länge aufweisen, enthält der andere Member nSize die Größe des Datensatzes. Unmittelbar nach dem nSize-Member sind die restlichen Parameter der GDI-Funktion, falls vorhanden. Der Rest der-Struktur enthält zusätzliche Daten, die vom Daten Satz Typen abhängig sind.

Der erste Datensatz in einer erweiterten Metadatei ist immer die [**enhmetaheader**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) -Struktur, die den Enhanced-Metadatei-Header darstellt. Der-Header gibt die folgenden Informationen an:

-   Größe der Metadatei in Bytes
-   Dimensionen des Bild Rahmens in Geräte Einheiten
-   Dimensionen des Bild Rahmens in. 01-Millimeter-Einheiten
-   Anzahl der Datensätze in der Metadatendatei
-   Offset für eine optionale Textbeschreibung
-   Größe der optionalen Palette
-   Auflösung des ursprünglichen Geräts in Pixel
-   Auflösung des ursprünglichen Geräts in Millimeter

Eine optionale Textbeschreibung kann dem Header Daten Satz folgen. In der Textbeschreibung werden das Bild und der Name des Autors beschrieben. Die optionale Palette gibt die Farben an, die zum Erstellen der erweiterten Metadatei verwendet werden. Die übrigen Datensätze identifizieren die GDI-Funktionen, die zum Erstellen des Bilds verwendet werden. Die folgende hexadezimale Ausgabe entspricht einem Datensatz, der für einen aufzurufenden Befehl der [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) -Funktion generiert wurde.


```C++
00000011 0000000C 00000004 
```



Der Wert 0x00000011 gibt den Daten Satz Typen an (entspricht der \_ in der Datei WinGDI. h definierten EMR setmapmode-Konstante). Der Wert 0x0000000c gibt die Länge des Datensatzes in Bytes an. Der Wert 0x00000004 identifiziert den Zuordnungs Modus (entspricht der \_ in der [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) -Funktion definierten mm-loenglish-Konstante).

Eine Liste der zusätzlichen Daten Satz Typen finden Sie unter [Metafile-Strukturen](metafile-structures.md).

 

 



