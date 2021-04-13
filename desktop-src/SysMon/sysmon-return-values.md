---
title: Sysmon-Rückgabewerte
description: Im folgenden finden Sie eine Liste der System Monitor-Rückgabewerte, die in smonmsg. h definiert sind.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390732"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="cb382-103">Sysmon-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cb382-103">SYSMON Return Values</span></span>

<span data-ttu-id="cb382-104">Im folgenden finden Sie eine Liste der System Monitor-Rückgabewerte, die in smonmsg. h definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cb382-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="cb382-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb382-105">Return value</span></span>                                       | <span data-ttu-id="cb382-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb382-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb382-107">Smon- \_ Status- \_ Dupl-Counter- \_ \_ Pfad (0xc0001388)</span><span class="sxs-lookup"><span data-stu-id="cb382-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="cb382-108">Die zählungssammlung enthält bereits den angegebenen Zählers.</span><span class="sxs-lookup"><span data-stu-id="cb382-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="cb382-109">Smon- \_ Status \_ kein \_ Sysmon- \_ Objekt (0xc0001389)</span><span class="sxs-lookup"><span data-stu-id="cb382-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="cb382-110">Die Einstellungen enthalten keine kompletten System Monitor-HTML-Objekte.</span><span class="sxs-lookup"><span data-stu-id="cb382-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="cb382-111">Smon- \_ Status \_ zu \_ wenige \_ Beispiele (0xc000138a)</span><span class="sxs-lookup"><span data-stu-id="cb382-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="cb382-112">Die angegebene Protokolldatei enthält weniger als zwei Daten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="cb382-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="cb382-113">Größenbeschränkung für smon- \_ Status \_ Protokoll \_ Datei \_ \_ (0xc000138b)</span><span class="sxs-lookup"><span data-stu-id="cb382-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="cb382-114">Die angegebene Protokolldatei überschreitet die Größenbeschränkungen des System Monitor-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="cb382-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="cb382-115">Wenn zurzeit eine Protokolldatei ausgewählt ist, wählen Sie aktuelle Aktivität als Datenquelle aus, um die aktuelle Protokolldatei zu entladen, und wählen Sie dann die angegebene Protokolldatei erneut aus.</span><span class="sxs-lookup"><span data-stu-id="cb382-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="cb382-116">Datenquelle für smon- \_ Status \_ Protokoll \_ Datei \_ \_ (0xc000138c)</span><span class="sxs-lookup"><span data-stu-id="cb382-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="cb382-117">Um der Datenquelle eine neue Protokolldatei hinzuzufügen, muss der Daten Quellentyp in einen anderen Typ als sysmonlogfiles geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cb382-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="cb382-118">Pfad für den smon- \_ Status der \_ \_ Protokoll \_ Datei \_ (0xc000138d)</span><span class="sxs-lookup"><span data-stu-id="cb382-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="cb382-119">Die Protokolldatei Sammlung enthält bereits die angegebene Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="cb382-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="cb382-120">Eine Beschreibung der zusätzlichen Rückgabewerte, die vom System Monitor zurückgegeben werden, finden Sie unter [System Fehlercodes](/windows/desktop/Debug/system-error-codes) und [Fehlercodes für Leistungsdaten](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="cb382-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 