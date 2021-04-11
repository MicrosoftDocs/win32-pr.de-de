---
description: Zeitbezogene Funktionen geben eine Zeit in einem von mehreren Formaten zurück. Sie können die Zeitfunktionen für die Konvertierung zwischen einigen Zeitformaten verwenden, um den Vergleich und die Anzeige zu vereinfachen. In der folgenden Tabelle werden die Zeitformate zusammengefasst.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Informationen zu Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042378"
---
# <a name="about-time"></a><span data-ttu-id="ae307-105">Informationen zu Zeit</span><span class="sxs-lookup"><span data-stu-id="ae307-105">About Time</span></span>

<span data-ttu-id="ae307-106">Zeitbezogene Funktionen geben eine Zeit in einem von mehreren Formaten zurück.</span><span class="sxs-lookup"><span data-stu-id="ae307-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="ae307-107">Sie können die Zeitfunktionen für die Konvertierung zwischen einigen Zeitformaten verwenden, um den Vergleich und die Anzeige zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="ae307-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="ae307-108">In der folgenden Tabelle werden die Zeitformate zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ae307-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="ae307-109">Format</span><span class="sxs-lookup"><span data-stu-id="ae307-109">Format</span></span>          | <span data-ttu-id="ae307-110">type</span><span class="sxs-lookup"><span data-stu-id="ae307-110">Type</span></span>                                                                     | <span data-ttu-id="ae307-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae307-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae307-112">System</span><span class="sxs-lookup"><span data-stu-id="ae307-112">System</span></span>          | [<span data-ttu-id="ae307-113">**System Time**</span><span class="sxs-lookup"><span data-stu-id="ae307-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="ae307-114">Jahr, Monat, Tag, Stunde, Sekunde und Millisekunde, die von der internen Hardware Uhr entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="ae307-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="ae307-115">Lokal</span><span class="sxs-lookup"><span data-stu-id="ae307-115">Local</span></span>           | <span data-ttu-id="ae307-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) oder [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="ae307-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="ae307-117">Eine Systemzeit-oder Dateizeit, die in die lokale Zeitzone des Systems konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ae307-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="ae307-118">File</span><span class="sxs-lookup"><span data-stu-id="ae307-118">File</span></span>            | [<span data-ttu-id="ae307-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="ae307-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="ae307-120">Die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="ae307-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="ae307-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="ae307-121">MS-DOS</span></span>          | <span data-ttu-id="ae307-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="ae307-122">**WORD**</span></span>                                                                 | <span data-ttu-id="ae307-123">Ein gepacktes Wort für das Datum, ein weiteres für die Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="ae307-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="ae307-124">Windows</span><span class="sxs-lookup"><span data-stu-id="ae307-124">Windows</span></span>         | <span data-ttu-id="ae307-125">**DWORD** oder **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="ae307-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="ae307-126">Die Anzahl der Millisekunden seit dem letzten Start des Systems.</span><span class="sxs-lookup"><span data-stu-id="ae307-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="ae307-127">Beim Abrufen als DWORD-Wert wird Windows-Zeitzyklen alle 49,7 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="ae307-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="ae307-128">Unterbrechungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="ae307-128">Interrupt Count</span></span> | <span data-ttu-id="ae307-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="ae307-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="ae307-130">Die Anzahl von 100-Nanosekunden-Intervallen seit dem letzten Start des Systems.</span><span class="sxs-lookup"><span data-stu-id="ae307-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="ae307-131">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ae307-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ae307-132">Systemzeit</span><span class="sxs-lookup"><span data-stu-id="ae307-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="ae307-133">Ortszeit</span><span class="sxs-lookup"><span data-stu-id="ae307-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="ae307-134">Datei Zeiten</span><span class="sxs-lookup"><span data-stu-id="ae307-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="ae307-135">Datum und Uhrzeit der MS-DOS</span><span class="sxs-lookup"><span data-stu-id="ae307-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="ae307-136">Windows-Zeitdienst</span><span class="sxs-lookup"><span data-stu-id="ae307-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="ae307-137">Interruptzeit</span><span class="sxs-lookup"><span data-stu-id="ae307-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
