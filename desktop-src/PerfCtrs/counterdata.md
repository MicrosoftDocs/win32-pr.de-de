---
description: Die Counter Data-Tabelle enthält eine Zeile für jeden Indikator, der zu einem bestimmten Zeitpunkt erfasst wird. Es wird eine große Anzahl dieser Zeilen angezeigt.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Gegen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865127"
---
# <a name="counterdata"></a><span data-ttu-id="871c5-104">Gegen Daten</span><span class="sxs-lookup"><span data-stu-id="871c5-104">CounterData</span></span>

<span data-ttu-id="871c5-105">Die **Counter Data** -Tabelle enthält eine Zeile für jeden Indikator, der zu einem bestimmten Zeitpunkt erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="871c5-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="871c5-106">Es wird eine große Anzahl dieser Zeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="871c5-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="871c5-107">Die **Counter Data** -Tabelle definiert die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="871c5-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="871c5-108">**GUID:** GUID für dieses DataSet.</span><span class="sxs-lookup"><span data-stu-id="871c5-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="871c5-109">Verwenden Sie diesen Schlüssel, um mit der [**displaytoid**](displaytoid.md) -Tabelle zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="871c5-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="871c5-110">**Counter ID:** Identifiziert den-Wert.</span><span class="sxs-lookup"><span data-stu-id="871c5-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="871c5-111">Verwenden Sie diesen Schlüssel, um mit der [**Counter Details**](counterdetails.md) -Tabelle zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="871c5-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="871c5-112">**RecordIndex:** Der Beispiel Index für einen bestimmten Indikator Bezeichner und eine Sammlungs-GUID.</span><span class="sxs-lookup"><span data-stu-id="871c5-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="871c5-113">Der Wert erhöht sich für jedes nachfolgende Beispiel in dieser Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="871c5-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="871c5-114">**Counterdatetime:** Der Zeitpunkt, zu dem die Sammlung gestartet wurde, in UTC-Zeit.</span><span class="sxs-lookup"><span data-stu-id="871c5-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="871c5-115">**CounterValue:** Der formatierte Wert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="871c5-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="871c5-116">Dieser Wert kann für den ersten Datensatz 0 (null) sein, wenn der Leistungs Besatz zwei Stichproben benötigt, um einen anzeigbaren Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="871c5-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="871c5-117">**Firstvaluea:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert von **firstvalueb** , um den **FirstValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="871c5-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="871c5-118">**Firstvaluea** enthält die Bits mit niedriger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="871c5-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="871c5-119">**Firstvalueb:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert von **firstvaluea** , um den **FirstValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="871c5-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="871c5-120">**Firstvalueb** enthält die hohen Bestell Bits.</span><span class="sxs-lookup"><span data-stu-id="871c5-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="871c5-121">**Secondvaluea:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **secondvalueb** , um den **SecondValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="871c5-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="871c5-122">**Secondvaluea** enthält die Bits mit niedriger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="871c5-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="871c5-123">**Secondvalueb:** Kombinieren Sie diesen 32-Bit-Wert mit dem Wert **secondvaluea** , um den **SecondValue** -Member des [**PDH- \_ rohleistungs \_ Zählers**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="871c5-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="871c5-124">**Secondvalueb** enthält die hohen Bestell Bits.</span><span class="sxs-lookup"><span data-stu-id="871c5-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="871c5-125">Die Felder **GUID**, **counterId** und **recordIndex** bilden den Primärschlüssel für diese Tabelle.</span><span class="sxs-lookup"><span data-stu-id="871c5-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



