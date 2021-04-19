---
description: Der Druck Spooler überwacht die aktuellen Druckaufträge und den Ziel Drucker, um eine geeignete Zeit zum Drucken eines Auftrags zu ermitteln.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Druck Prozessor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347997"
---
# <a name="print-processor"></a><span data-ttu-id="2bb86-103">Druck Prozessor</span><span class="sxs-lookup"><span data-stu-id="2bb86-103">Print Processor</span></span>

<span data-ttu-id="2bb86-104">Der Druck Spooler überwacht die aktuellen Druckaufträge und den Ziel Drucker, um eine geeignete Zeit zum Drucken eines Auftrags zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2bb86-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="2bb86-105">Wenn der Spooler feststellt, dass ein Auftrag gedruckt werden soll, ruft er den Druck Prozessor auf.</span><span class="sxs-lookup"><span data-stu-id="2bb86-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="2bb86-106">Der Druck Prozessor ist ein Plug-in, das Druckauftrags Daten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2bb86-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="2bb86-107">Verwenden Sie die folgenden Funktionen, um mit Druck Prozessoren zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2bb86-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="2bb86-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="2bb86-108">Function</span></span>                                                           | <span data-ttu-id="2bb86-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bb86-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="2bb86-110">**Addprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="2bb86-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="2bb86-111">Installiert einen Druck Prozessor auf einem angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="2bb86-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="2bb86-112">**Deleteprintprocessor**</span><span class="sxs-lookup"><span data-stu-id="2bb86-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="2bb86-113">Entfernt einen Drucker Prozessor von einem angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="2bb86-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="2bb86-114">**Enumprintprocessordatatypes**</span><span class="sxs-lookup"><span data-stu-id="2bb86-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="2bb86-115">Listet die Datentypen auf, die ein angegebener Druck Prozessor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2bb86-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="2bb86-116">**Enumprintprozessoren**</span><span class="sxs-lookup"><span data-stu-id="2bb86-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="2bb86-117">Listet die Druck Prozessoren auf, die auf einem angegebenen Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="2bb86-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="2bb86-118">**Getprintprocessordirectory**</span><span class="sxs-lookup"><span data-stu-id="2bb86-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="2bb86-119">Ruft den Pfad für den Druck Prozessor auf dem angegebenen Server ab.</span><span class="sxs-lookup"><span data-stu-id="2bb86-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



