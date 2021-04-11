---
description: Fügen Sie der Tabelle CustomAction einen Datensatz für die Aktion benutzerdefinierte Aktion starten hinzu.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Hinzufügen von Start zu den Tabellen CustomAction und Binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131505"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="3749a-103">Hinzufügen von Start zu den Tabellen CustomAction und Binary</span><span class="sxs-lookup"><span data-stu-id="3749a-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="3749a-104">Fügen Sie der [Tabelle CustomAction](customaction-table.md) einen Datensatz für die Aktion benutzerdefinierte Aktion starten hinzu.</span><span class="sxs-lookup"><span data-stu-id="3749a-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="3749a-105">Geben Sie den Namen der benutzerdefinierten Aktion in der Spalte Aktion der Tabelle CustomAction ein.</span><span class="sxs-lookup"><span data-stu-id="3749a-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="3749a-106">Geben Sie den gesamten numerischen Typ für Launch, 65 in die Spalte Type der Tabelle Custom Action ein.</span><span class="sxs-lookup"><span data-stu-id="3749a-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="3749a-107">Die Quell Spalte der Tabelle CustomAction gibt einen Schlüssel in den Datensatz der [binären Tabelle](binary-table.md) an, die die Binärdaten für die dll enthält.</span><span class="sxs-lookup"><span data-stu-id="3749a-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="3749a-108">Geben Sie Tutorial.dll in die Spalte Quelle der Tabelle CustomAction ein.</span><span class="sxs-lookup"><span data-stu-id="3749a-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="3749a-109">Der Einstiegspunkt, der im Zielfeld der CustomAction-Tabelle angegeben ist, muss mit dem aus der DLL exportierten Eintrag identisch sein.</span><span class="sxs-lookup"><span data-stu-id="3749a-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="3749a-110">Geben Sie launchtutorial in die Ziel Spalte der Tabelle CustomAction ein.</span><span class="sxs-lookup"><span data-stu-id="3749a-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="3749a-111">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="3749a-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="3749a-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="3749a-112">Action</span></span> | <span data-ttu-id="3749a-113">type</span><span class="sxs-lookup"><span data-stu-id="3749a-113">Type</span></span> | <span data-ttu-id="3749a-114">`Source`</span><span class="sxs-lookup"><span data-stu-id="3749a-114">Source</span></span>       | <span data-ttu-id="3749a-115">Ziel</span><span class="sxs-lookup"><span data-stu-id="3749a-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="3749a-116">Starten</span><span class="sxs-lookup"><span data-stu-id="3749a-116">Launch</span></span> | <span data-ttu-id="3749a-117">65</span><span class="sxs-lookup"><span data-stu-id="3749a-117">65</span></span>   | <span data-ttu-id="3749a-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="3749a-118">Tutorial.dll</span></span> | <span data-ttu-id="3749a-119">Launchtutorial</span><span class="sxs-lookup"><span data-stu-id="3749a-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="3749a-120">Fügen Sie die Tutorial.dll, die Sie aus Tutorial. cpp erstellt haben, als binären Stream zur binären Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="3749a-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="3749a-121">Binäre Tabelle</span><span class="sxs-lookup"><span data-stu-id="3749a-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="3749a-122">Name</span><span class="sxs-lookup"><span data-stu-id="3749a-122">Name</span></span>         | <span data-ttu-id="3749a-123">Daten</span><span class="sxs-lookup"><span data-stu-id="3749a-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="3749a-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="3749a-124">Tutorial.dll</span></span> | <span data-ttu-id="3749a-125">{*binäre Daten für dll-Datei hinzugefügt*</span><span class="sxs-lookup"><span data-stu-id="3749a-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="3749a-126">Fügen Sie [am Ende der Installation ein Steuerungs Ereignis hinzu, um den Start auszuführen](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="3749a-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



