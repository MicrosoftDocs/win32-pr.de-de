---
description: Die Installer-Funktionen können verwendet werden, um bestimmte Aktionen oder Aktions Sequenzen auszuführen.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Ausführen von Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343398"
---
# <a name="running-actions"></a><span data-ttu-id="8674d-103">Ausführen von Aktionen</span><span class="sxs-lookup"><span data-stu-id="8674d-103">Running Actions</span></span>

<span data-ttu-id="8674d-104">Die Installer-Funktionen können verwendet werden, um bestimmte Aktionen oder Aktions Sequenzen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8674d-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="8674d-105">Diese Aktionen können entweder [standardmäßige](standard-actions.md) oder [benutzerdefinierte](custom-actions.md) Aktionen sein.</span><span class="sxs-lookup"><span data-stu-id="8674d-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="8674d-106">Im folgenden Verfahren wird beschrieben, wie Sie Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="8674d-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="8674d-107">**So führen Sie eine Aktions Sequenz aus**</span><span class="sxs-lookup"><span data-stu-id="8674d-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="8674d-108">Führen Sie eine Sequenz von Aktionen aus, die in einer Tabelle durch Aufrufen der [**msisequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) -Funktion definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8674d-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="8674d-109">Das Installationsprogramm fragt die entsprechende Tabelle ab und führt jede Aktion aus, wenn der bedingte Ausdruck true ergibt.</span><span class="sxs-lookup"><span data-stu-id="8674d-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="8674d-110">Überprüfen Sie bedingte Ausdrücke, indem Sie die [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8674d-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="8674d-111">Führen Sie die Aktion aus, indem Sie die [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8674d-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="8674d-112">Bei der Aktion kann es sich um eine Standardaktion, eine benutzerdefinierte Aktion oder ein Benutzeroberflächen Dialogfeld handeln.</span><span class="sxs-lookup"><span data-stu-id="8674d-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="8674d-113">Wenn während der Ausführung dieser Aktion ein Fehler aufgetreten ist, wird die [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8674d-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="8674d-114">Der Fehler wird vom Installationsprogramm verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8674d-114">The installer will process the error.</span></span>

 

 



