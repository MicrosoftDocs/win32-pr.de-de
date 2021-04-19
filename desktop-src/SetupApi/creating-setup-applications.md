---
description: Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für die Setup Anwendung. Sie müssen die Setup Funktionen von der Setup Anwendung aus ausführen, um viele Installations Vorgänge auszuführen.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Erstellen von Setup Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373156"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="3a75e-104">Erstellen von Setup Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3a75e-104">Creating Setup Applications</span></span>

<span data-ttu-id="3a75e-105">Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für die Setup Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3a75e-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="3a75e-106">Sie müssen die Setup Funktionen von der Setup Anwendung aus ausführen, um viele Installations Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3a75e-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="3a75e-107">In den folgenden Schritten wird eine Möglichkeit behandelt, mit den Setup Funktionen eine Setup Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a75e-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="3a75e-108">Sie können dieses Beispiel als Ausgangspunkt verwenden oder einen eigenen Installations Algorithmus entwickeln.</span><span class="sxs-lookup"><span data-stu-id="3a75e-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="3a75e-109">**Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="3a75e-109">**Initialization**</span></span>

-   [<span data-ttu-id="3a75e-110">Öffnen Sie die INF-Datei, und fügen Sie ggf. andere INF-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="3a75e-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="3a75e-111">Extrahieren Sie Dateiinformationen aus der INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="3a75e-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="3a75e-112">Sammeln Sie Setup Informationen vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3a75e-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="3a75e-113">Erstellen Sie eine Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="3a75e-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="3a75e-114">**Dateien installieren**</span><span class="sxs-lookup"><span data-stu-id="3a75e-114">**Install files**</span></span>

-   [<span data-ttu-id="3a75e-115">Commit für die Warteschlange, wobei eine Rückruf Routine angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a75e-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="3a75e-116">Aktualisieren von Registrierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="3a75e-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="3a75e-117">**Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="3a75e-117">**Clean up**</span></span>

-   [<span data-ttu-id="3a75e-118">Schließen Sie die Datei Warteschlange und inf.</span><span class="sxs-lookup"><span data-stu-id="3a75e-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="3a75e-119">Geben Sie alle anderen Systemressourcen frei, und beenden Sie das Programm.</span><span class="sxs-lookup"><span data-stu-id="3a75e-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



