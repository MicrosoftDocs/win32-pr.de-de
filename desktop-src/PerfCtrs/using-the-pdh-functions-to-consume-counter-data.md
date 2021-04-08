---
description: Sie verwenden die PDH-Funktionen, um Leistungsdaten zu erfassen.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Verwenden der PDH-Funktionen zum Verarbeiten von Counter-Daten
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865088"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="749ec-103">Verwenden der PDH-Funktionen zum Verarbeiten von Counter-Daten</span><span class="sxs-lookup"><span data-stu-id="749ec-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="749ec-104">Verwenden Sie die PDH-Funktionen, um Leistungsdaten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="749ec-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="749ec-105">Die PDH-Funktionen sind einfacher zu verwenden als die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) und können verwendet werden, um auf die Daten des Dienstanbietern v1 und v2 zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="749ec-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="749ec-106">PDH verfügt über APIs zum Erfassen aktueller Leistungsdaten, zum Speichern von Leistungsdaten in Protokolldateien und zum Lesen von Daten aus Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="749ec-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="749ec-107">Wenn Sie Windows onecore-apps schreiben, können Sie die Funktionen für die Abstraktionsschicht der Leistungsdaten nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="749ec-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="749ec-108">Verwenden Sie stattdessen [Perflib v2-consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md).</span><span class="sxs-lookup"><span data-stu-id="749ec-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="749ec-109">PDH ist eine API auf hoher Ebene, die das Sammeln von Leistungsdaten für Leistungsdaten vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="749ec-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="749ec-110">Es unterstützt die Abfrage Verarbeitung, das Zwischenspeichern von Metadaten, das Zuordnen von Instanzen zwischen Beispielen, das berechnen formatierter Werte aus unformatierten Werten, das Lesen von Daten aus Protokolldateien und das Speichern von Daten in Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="749ec-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="749ec-111">PDH verwendet automatisch die [Registrierungsfunktionen](using-the-registry-functions-to-consume-counter-data.md) beim Sammeln von Daten von **v1-Anbietern** und verwendet die V2- [consumerfunktionen](using-the-perflib-functions-to-consume-counter-data.md) beim Sammeln von Daten von **v2-Anbietern**.</span><span class="sxs-lookup"><span data-stu-id="749ec-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="749ec-112">Führen Sie die folgenden Schritte aus, um Leistungsdaten mithilfe der PDH-Funktionen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="749ec-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="749ec-113">Erstellen einer Abfrage</span><span class="sxs-lookup"><span data-stu-id="749ec-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="749ec-114">Zähler zur Abfrage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="749ec-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="749ec-115">Erfassen der Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="749ec-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="749ec-116">Anzeigen der Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="749ec-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="749ec-117">Schließen der Abfrage</span><span class="sxs-lookup"><span data-stu-id="749ec-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="749ec-118">Sie können Leistungsdaten entweder aus echtzeitquellen oder Protokolldateien erfassen.</span><span class="sxs-lookup"><span data-stu-id="749ec-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="749ec-119">Weitere Informationen zum Schreiben von Leistungsdaten in Protokolldateien finden Sie unter [Arbeiten mit Protokolldateien](working-with-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="749ec-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="749ec-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="749ec-120">See also</span></span>

- [<span data-ttu-id="749ec-121">Sammeln von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="749ec-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="749ec-122">Leistungsindikatoren durchsuchen</span><span class="sxs-lookup"><span data-stu-id="749ec-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="749ec-123">Rückgabewerte der PDH-Schnittstelle werden überprüft</span><span class="sxs-lookup"><span data-stu-id="749ec-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="749ec-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="749ec-124">Examples</span></span>](examples.md)
