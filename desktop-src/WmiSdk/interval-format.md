---
description: Definiert Datums-/uhrzeitintervalle mit einem Format, das der Datums-und Uhrzeit Syntax ähnelt, indem die Zeichenfolge in die Felder für Tage, Stunden, Minuten, Sekunden und Mikrosekunden aufgeteilt wird.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Intervall Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357069"
---
# <a name="interval-format"></a><span data-ttu-id="60127-103">Intervall Format</span><span class="sxs-lookup"><span data-stu-id="60127-103">Interval Format</span></span>

<span data-ttu-id="60127-104">WMI definiert Datums-/uhrzeitintervalle mit einem Format, das der Datums-und Uhrzeit Syntax ähnelt, indem die Zeichenfolge in die Felder für Tage, Stunden, Minuten, Sekunden und Mikrosekunden aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="60127-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="60127-105">Das folgende Beispiel zeigt das Format eines Datums-/uhrzeitintervalls.</span><span class="sxs-lookup"><span data-stu-id="60127-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="60127-106">In der folgenden Tabelle sind die Felder des Datums-/uhrzeitintervalls aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="60127-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="60127-107">Feld</span><span class="sxs-lookup"><span data-stu-id="60127-107">Field</span></span>    | <span data-ttu-id="60127-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60127-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60127-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="60127-109">dddddddd</span></span> | <span data-ttu-id="60127-110">Acht Ziffern, die eine Anzahl von Tagen darstellen (00000000 bis 99999999).</span><span class="sxs-lookup"><span data-stu-id="60127-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="60127-111">HH</span><span class="sxs-lookup"><span data-stu-id="60127-111">HH</span></span>       | <span data-ttu-id="60127-112">Zweistellige Stunden Angabe des Tages, bei dem das 24-Stunden-Format (00 bis 23) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60127-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="60127-113">MM</span><span class="sxs-lookup"><span data-stu-id="60127-113">MM</span></span>       | <span data-ttu-id="60127-114">Zweistellige Minuten Angabe in der Stunde (00 bis 59).</span><span class="sxs-lookup"><span data-stu-id="60127-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="60127-115">SS</span><span class="sxs-lookup"><span data-stu-id="60127-115">SS</span></span>       | <span data-ttu-id="60127-116">Zweistellige Anzahl von Sekunden in der Minute (00 bis 59).</span><span class="sxs-lookup"><span data-stu-id="60127-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="60127-117">mmmmmm</span><span class="sxs-lookup"><span data-stu-id="60127-117">mmmmmm</span></span>   | <span data-ttu-id="60127-118">Sechsstellige Anzahl von Mikrosekunden im zweiten Wert (000000 bis 999999).</span><span class="sxs-lookup"><span data-stu-id="60127-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="60127-119">Ihre Implementierung ist nicht erforderlich, um die Auswertung mit diesem Feld zu unterstützen, aber dieses Feld muss immer vorhanden sein, um die Länge der Zeichenfolge mit fester Länge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="60127-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="60127-120">Intervalle verfügen immer über eine nachfolgende ": 000"-in den letzten vier Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60127-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="60127-121">Darüber hinaus können Sie im Gegensatz zu Datum und Uhrzeit nicht verwendete Felder mithilfe von Sternchen angeben.</span><span class="sxs-lookup"><span data-stu-id="60127-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="60127-122">Außerdem müssen alle Eigenschaften vom Typ [CIM \_ DateTime](cim-datetime.md) , die Intervalle darstellen, mit dem [Untertyp](standard-wmi-qualifiers.md) Standard Qualifizierer gekennzeichnet werden, wobei der Qualifizierer auf "Interval" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60127-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="60127-123">Die folgende Zeichenfolge stellt ein Intervall von 1 Tag, 12 Stunden, 0 Minuten und 32 Sekunden dar.</span><span class="sxs-lookup"><span data-stu-id="60127-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="60127-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60127-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60127-125">Datums-und Uhrzeit Format</span><span class="sxs-lookup"><span data-stu-id="60127-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="60127-126">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="60127-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="60127-127">CIM- \_ DateTime</span><span class="sxs-lookup"><span data-stu-id="60127-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



