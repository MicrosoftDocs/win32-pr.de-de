---
description: Beschreibt Zeitformate, die für die Verwendung in der WQL WHERE-Klausel unterstützt werden.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported Zeitformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368234"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="97d32-103">WQL-Supported Zeitformate</span><span class="sxs-lookup"><span data-stu-id="97d32-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="97d32-104">Zusätzlich zum WMI-DateTime-Format werden die folgenden Datumsformate für die Verwendung in der WQL-WHERE-Klausel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97d32-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="97d32-105">Format</span><span class="sxs-lookup"><span data-stu-id="97d32-105">Format</span></span>                                    | <span data-ttu-id="97d32-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97d32-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d32-107">HH \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="97d32-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="97d32-108">Stunde, wie in einer zwölfstündigen Uhr und am-oder PM-Bezeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="97d32-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="97d32-109">4 PM</span><span class="sxs-lookup"><span data-stu-id="97d32-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="97d32-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="97d32-110">hh:mm</span></span><br/>                          | <span data-ttu-id="97d32-111">Durch Trennzeichen getrennte Stunde und Minuten.</span><span class="sxs-lookup"><span data-stu-id="97d32-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="97d32-112">Keine am-oder PM-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="97d32-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="97d32-113">3:23</span><span class="sxs-lookup"><span data-stu-id="97d32-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="97d32-114">hh: mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="97d32-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="97d32-115">Durch Trennzeichen getrennte Stunde und Minuten, optionaler Raum und am-oder PM-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="97d32-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="97d32-116">3:23 Uhr</span><span class="sxs-lookup"><span data-stu-id="97d32-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="97d32-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="97d32-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="97d32-118">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden.</span><span class="sxs-lookup"><span data-stu-id="97d32-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="97d32-119">Keine am/pm-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="97d32-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="97d32-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="97d32-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="97d32-121">hh: mm: SS \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="97d32-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="97d32-122">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden, Optionaler Leerraum und am/pm-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="97d32-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="97d32-123">3:23 Uhr</span><span class="sxs-lookup"><span data-stu-id="97d32-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="97d32-124">hh: mm: SS: uuu</span><span class="sxs-lookup"><span data-stu-id="97d32-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="97d32-125">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden und ein dreistelliger Offset, das die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.</span><span class="sxs-lookup"><span data-stu-id="97d32-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="97d32-126">hh: mm: SS: \[ \[ u \] u \] u</span><span class="sxs-lookup"><span data-stu-id="97d32-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="97d32-127">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden. und einen, zwei oder dreistelligen Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht.</span><span class="sxs-lookup"><span data-stu-id="97d32-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="97d32-128">hh: mm: SS: uuu \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="97d32-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="97d32-129">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden, ein dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC und am oder PM-Bezeichnung abweicht.</span><span class="sxs-lookup"><span data-stu-id="97d32-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="97d32-130">hh: mm: SS: \[ \[ u \] u \] \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="97d32-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="97d32-131">Durch Trennzeichen getrennte Stunde, Minuten und Sekunden. ein-, zwei-oder dreistelliger Offset, der die Anzahl der Minuten angibt, die die ursprüngliche Zeitzone von UTC abweicht. und am-oder PM-Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="97d32-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="97d32-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97d32-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d32-133">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="97d32-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




