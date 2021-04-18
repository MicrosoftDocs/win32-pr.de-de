---
description: Einschränkungen für das Beispielprogramm
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Einschränkungen für das Beispielprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347715"
---
# <a name="example-program-limitations"></a><span data-ttu-id="f6026-103">Einschränkungen für das Beispielprogramm</span><span class="sxs-lookup"><span data-stu-id="f6026-103">Example Program Limitations</span></span>

<span data-ttu-id="f6026-104">Grundsätze von guten Programmierpraktiken sind nicht immer in diesen Beispielprogrammen befolgt, um präziseren, besser lesbaren Code bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f6026-104">Principles of good programming practice are not always followed in these sample programs in order to provide more concise, more readable code.</span></span> <span data-ttu-id="f6026-105">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="f6026-105">In particular:</span></span>

-   <span data-ttu-id="f6026-106">Nur eingeschränkte Fehler Antworten werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6026-106">Only limited error responses are shown.</span></span> <span data-ttu-id="f6026-107">Bei funktionierenden Programmen sollten immer zurückgegebene Fehlercodes überprüft und geeignete Aktionen durchgeführt werden, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f6026-107">Working programs should always check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="f6026-108">Nur eingeschränkte Arbeitsspeicher-und Ressourcenverwaltung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f6026-108">Only limited memory and resource management is done.</span></span> <span data-ttu-id="f6026-109">In Arbeitsprogrammen sollten alle Schlüssel und [*Hashes*](../secgloss/h-gly.md) zerstört werden, der gesamte zugeordnete Arbeitsspeicher muss freigegeben werden, alle Dateien sollten geschlossen werden, und alle Handles sollten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6026-109">In working programs, all keys and [*hashes*](../secgloss/h-gly.md) should be destroyed, all allocated memory should be freed, all files should be closed, and all handles should be released.</span></span> <span data-ttu-id="f6026-110">Diese Beispiel Programme bieten nur eine begrenzte Demonstration der Verwendung von Funktionen, die diese Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6026-110">These example programs provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="f6026-111">Diese Beispiel Programme führen keine Arbeitsspeicher-oder Ressourcen Verwaltungsaufgaben aus, wenn die Programm Beendigung aufgrund von Fehlern auftritt.</span><span class="sxs-lookup"><span data-stu-id="f6026-111">These example programs perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

 

 
