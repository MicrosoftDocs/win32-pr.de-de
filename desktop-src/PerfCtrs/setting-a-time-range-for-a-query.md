---
description: Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, können Sie einen Zeitbereich für die Abfrage angeben.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Festlegen eines Zeit Bereichs für eine Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357753"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="ffa8a-103">Festlegen eines Zeit Bereichs für eine Abfrage</span><span class="sxs-lookup"><span data-stu-id="ffa8a-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="ffa8a-104">Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, können Sie einen Zeitbereich für die Abfrage angeben.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="ffa8a-105">Die Abfrage ruft Leistungsdaten aus der Protokolldatei ab, die während des angegebenen Zeitraums erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="ffa8a-106">Um den Zeitbereich festzulegen, müssen Sie die [**pdhsetquerytimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="ffa8a-107">**Pdhsetquerytimerange** wird nicht verwendet, um Leistungsdaten aus Echtzeitdaten Quellen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="ffa8a-108">Führen Sie die folgenden Schritte aus, um einen Zeitwert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="ffa8a-109">Weisen Sie eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zu, und initialisieren Sie die Felder mit dem gewünschten Uhrzeitwert.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="ffa8a-110">Ruft [**systemtimeyfiletime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) auf, um den Zeitwert der [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur in eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur Zeit zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="ffa8a-111">Wandeln Sie die [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur als Longlong-Variable um, wobei Sie die Auffüll Konventionen für Strukturelemente ihrer Plattform und Ihres Compilers berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="ffa8a-112">Kopieren Sie den Longlong-Wert in das entsprechende Feld in der [**PDH- \_ Zeit \_ Info**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="ffa8a-113">Rufen Sie die [**pdhgetdatasourcetimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) -Funktion auf, um den Zeitbereich aller in einer Protokolldatei enthaltenen Leistungsdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ffa8a-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
