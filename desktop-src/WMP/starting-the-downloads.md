---
title: Starten der Downloads
description: Starten der Downloads
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Downloads starten
- Online Stores, Downloads starten
- Typ 2 Online Stores, Downloads starten
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Downloads werden gestartet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388692"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="0b394-113">Starten der Downloads</span><span class="sxs-lookup"><span data-stu-id="0b394-113">Starting the Downloads</span></span>

<span data-ttu-id="0b394-114">Der Download beginnt, wenn der Benutzer auf **herunterladen** klickt.</span><span class="sxs-lookup"><span data-stu-id="0b394-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="0b394-115">Diese Schaltfläche wird im Code btndownload genannt, und die Ereignishandlerfunktion für das **OnClick** -Ereignis heißt "ondownload".</span><span class="sxs-lookup"><span data-stu-id="0b394-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="0b394-116">"Ondownload" erstellt zunächst ein neues leeres **downloadcollection** -Objekt und weist es einer lokalen Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="0b394-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="0b394-117">Im nächsten Schritt startet die Funktion jedes der fünf Elemente, die heruntergeladen werden, und speichert das zurückgegebene " **downloadaditem** "-Objekt in einem Array.</span><span class="sxs-lookup"><span data-stu-id="0b394-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="0b394-118">Der Code aktualisiert dann die Elemente der Benutzeroberfläche mit den Informationen zur Download Auflistung und Ihren Download Elementen.</span><span class="sxs-lookup"><span data-stu-id="0b394-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b394-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b394-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b394-120">**Verwenden des Download-Managers**</span><span class="sxs-lookup"><span data-stu-id="0b394-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




