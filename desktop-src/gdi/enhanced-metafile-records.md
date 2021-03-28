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
# <a name="enhanced-metafile-records"></a><span data-ttu-id="c0b5b-103">Erweiterte Metafile-Datensätze</span><span class="sxs-lookup"><span data-stu-id="c0b5b-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="c0b5b-104">Eine erweiterte Metadatei ist ein Array von Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="c0b5b-105">Ein Metadateidatensatz ist eine " [**enhmetarecord**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) "-Struktur mit variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="c0b5b-106">Am Anfang jedes erweiterten Metadateidatensatz ist eine [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) -Struktur, die zwei Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="c0b5b-107">Der erste Member, ITYPE, identifiziert den Daten Satz Typen, d. h. die GDI-Funktion, deren Parameter im Datensatz enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="c0b5b-108">Da die-Strukturen eine Variable Länge aufweisen, enthält der andere Member nSize die Größe des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="c0b5b-109">Unmittelbar nach dem nSize-Member sind die restlichen Parameter der GDI-Funktion, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="c0b5b-110">Der Rest der-Struktur enthält zusätzliche Daten, die vom Daten Satz Typen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="c0b5b-111">Der erste Datensatz in einer erweiterten Metadatei ist immer die [**enhmetaheader**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) -Struktur, die den Enhanced-Metadatei-Header darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="c0b5b-112">Der-Header gibt die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="c0b5b-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="c0b5b-113">Größe der Metadatei in Bytes</span><span class="sxs-lookup"><span data-stu-id="c0b5b-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="c0b5b-114">Dimensionen des Bild Rahmens in Geräte Einheiten</span><span class="sxs-lookup"><span data-stu-id="c0b5b-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="c0b5b-115">Dimensionen des Bild Rahmens in. 01-Millimeter-Einheiten</span><span class="sxs-lookup"><span data-stu-id="c0b5b-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="c0b5b-116">Anzahl der Datensätze in der Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="c0b5b-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="c0b5b-117">Offset für eine optionale Textbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c0b5b-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="c0b5b-118">Größe der optionalen Palette</span><span class="sxs-lookup"><span data-stu-id="c0b5b-118">Size of the optional palette</span></span>
-   <span data-ttu-id="c0b5b-119">Auflösung des ursprünglichen Geräts in Pixel</span><span class="sxs-lookup"><span data-stu-id="c0b5b-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="c0b5b-120">Auflösung des ursprünglichen Geräts in Millimeter</span><span class="sxs-lookup"><span data-stu-id="c0b5b-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="c0b5b-121">Eine optionale Textbeschreibung kann dem Header Daten Satz folgen.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="c0b5b-122">In der Textbeschreibung werden das Bild und der Name des Autors beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="c0b5b-123">Die optionale Palette gibt die Farben an, die zum Erstellen der erweiterten Metadatei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="c0b5b-124">Die übrigen Datensätze identifizieren die GDI-Funktionen, die zum Erstellen des Bilds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="c0b5b-125">Die folgende hexadezimale Ausgabe entspricht einem Datensatz, der für einen aufzurufenden Befehl der [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) -Funktion generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="c0b5b-126">Der Wert 0x00000011 gibt den Daten Satz Typen an (entspricht der \_ in der Datei WinGDI. h definierten EMR setmapmode-Konstante).</span><span class="sxs-lookup"><span data-stu-id="c0b5b-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="c0b5b-127">Der Wert 0x0000000c gibt die Länge des Datensatzes in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="c0b5b-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="c0b5b-128">Der Wert 0x00000004 identifiziert den Zuordnungs Modus (entspricht der \_ in der [**setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) -Funktion definierten mm-loenglish-Konstante).</span><span class="sxs-lookup"><span data-stu-id="c0b5b-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="c0b5b-129">Eine Liste der zusätzlichen Daten Satz Typen finden Sie unter [Metafile-Strukturen](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c0b5b-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



