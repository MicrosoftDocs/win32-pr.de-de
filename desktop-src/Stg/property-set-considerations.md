---
title: Überlegungen zu Eigenschaften Gruppen
description: Es wird dringend empfohlen, dass Eigenschaften Sätze klein gehalten werden, da der Eigenschaften Satz-Stream in den Arbeitsspeicher gelesen wird, bevor eine einzelne Eigenschaft gelesen oder geschrieben werden kann.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Überlegungen zu Eigenschaften Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714561"
---
# <a name="property-set-considerations"></a><span data-ttu-id="6431d-104">Überlegungen zu Eigenschaften Gruppen</span><span class="sxs-lookup"><span data-stu-id="6431d-104">Property Set Considerations</span></span>

<span data-ttu-id="6431d-105">Es wird dringend empfohlen, dass Eigenschaften Sätze klein gehalten werden, da der Eigenschaften Satz-Stream in den Arbeitsspeicher gelesen wird, bevor eine einzelne Eigenschaft gelesen oder geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6431d-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="6431d-106">"Small" bedeutet weniger als 32 Kilobyte an Daten.</span><span class="sxs-lookup"><span data-stu-id="6431d-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="6431d-107">Dies stellt selten ein Problem dar, da in der Regel "Inline" Eigenschaften kleine Elemente wie beschreibende Zeichen folgen, Schlüsselwörter, Zeitstempel, Zahlen, Autorennamen, global eindeutige Bezeichner (GUIDs), Klassen Bezeichner (CLSIDs) usw. sein werden.</span><span class="sxs-lookup"><span data-stu-id="6431d-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="6431d-108">Zum Speichern größerer Datenblöcke oder in Fällen, in denen die Gesamtgröße eines Satzes verwandter Eigenschaften den empfohlenen Betrag überschreitet, wird dringend empfohlen, nicht einfache Typen wie z. b. **VT \_ Stream** und **VT- \_ Speicher** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6431d-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="6431d-109">Diese werden nicht im Eigenschaften Satz-Stream gespeichert, sodass Sie nicht maßgeblich den anfänglichen mehr Aufwand des ersten Zugriffs und Schreibens einer Eigenschaft beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="6431d-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="6431d-110">Da der Eigenschafts Satz-Stream den Namen des gleich geordneten Streams oder der Speicher Wert Eigenschaft enthält, ist ein minimaler mehr Aufwand erforderlich, da der Wert für die Verarbeitung etwas geringer ist.</span><span class="sxs-lookup"><span data-stu-id="6431d-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="6431d-111">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="6431d-111">For more information, see:</span></span>

-   [<span data-ttu-id="6431d-112">Überlegungen zur IPropertySetStorage-Implementierung</span><span class="sxs-lookup"><span data-stu-id="6431d-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="6431d-113">Speichern von Eigenschafts Sätzen</span><span class="sxs-lookup"><span data-stu-id="6431d-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="6431d-114">Leistungsmerkmale</span><span class="sxs-lookup"><span data-stu-id="6431d-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="6431d-115">Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen</span><span class="sxs-lookup"><span data-stu-id="6431d-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




