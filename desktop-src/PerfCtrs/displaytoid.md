---
description: Die displaytoid-Tabelle bezieht die vom System Monitor angezeigte benutzerfreundliche Zeichenfolge auf die GUID, die in den anderen Tabellen gespeichert ist.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: Display toid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347367"
---
# <a name="displaytoid"></a><span data-ttu-id="d7e74-103">Display toid</span><span class="sxs-lookup"><span data-stu-id="d7e74-103">DisplayToID</span></span>

<span data-ttu-id="d7e74-104">Die **displaytoid** -Tabelle bezieht die vom System Monitor angezeigte benutzerfreundliche Zeichenfolge auf die GUID, die in den anderen Tabellen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d7e74-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="d7e74-105">Die Tabelle **displaytoid** definiert die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="d7e74-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="d7e74-106">**GUID:** Eindeutiger Bezeichner, der für ein Protokoll generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e74-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="d7e74-107">Dieses Feld ist der Primärschlüssel dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d7e74-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="d7e74-108">**RunId:** Reserviert für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="d7e74-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="d7e74-109">**Display String:** Der Name der Protokolldatei, wie im System Monitor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7e74-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="d7e74-110">**Logstarttime:** Zeitpunkt, zu dem der Protokollierungs Prozess im Format yyyy-mm-dd hh: mm: SS: nnn gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e74-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="d7e74-111">**Logstoptime:** Zeitpunkt, zu dem der Protokollierungs Prozess im Format yyyy-mm-dd hh: mm: SS: nnn beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e74-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="d7e74-112">Mehrere Protokolldateien mit demselben **DisplayString** -Wert können unterschieden werden, indem Sie den Wert in diesem und den **logstarttime** -Feldern verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7e74-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="d7e74-113">Mit den Werten in den Feldern **logstarttime** und **logstoptime** kann auch schnell auf die gesamte Sammlungszeit zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="d7e74-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="d7e74-114">**Anzahl von Datensätzen:** Anzahl von Samplings, die in der Tabelle für jede Protokoll Sammlung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d7e74-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="d7e74-115">**Minutestoutc:** Der Wert, der verwendet wird, um die in UTC-Zeit gespeicherten Zeilendaten in die Ortszeit zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d7e74-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="d7e74-116">**TimeZoneName:** Der Name der Zeitzone, in der die Daten erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="d7e74-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="d7e74-117">Wenn Sie Daten aus einer Datei sammeln oder erneut protokolliert haben, die auf Systemen in ihrer eigenen Zeitzone gesammelt wurde, wird in diesem Feld der Speicherort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7e74-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="d7e74-118">**Hinweis**  Vor Windows Vista wurden die Datensammler Sätze in der Registrierung unter gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d7e74-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="d7e74-119">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog- \\ Protokoll Abfragen**</span><span class="sxs-lookup"><span data-stu-id="d7e74-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="d7e74-120">.</span><span class="sxs-lookup"><span data-stu-id="d7e74-120">.</span></span> <span data-ttu-id="d7e74-121">Die oben aufgeführten Felder entsprechen nicht den Werten in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d7e74-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="d7e74-122">Für Windows Vista werden die Datensammler Sätze nicht in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d7e74-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



