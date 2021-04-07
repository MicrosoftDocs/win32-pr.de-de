---
title: Abrufen von Status Informationen
description: Abrufen von Status Informationen
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Abrufen des Status
- Online Stores, Abrufen des Status
- Typ 2 Online Stores, Status abrufen
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Abrufen des Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712720"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="132e3-113">Abrufen von Status Informationen</span><span class="sxs-lookup"><span data-stu-id="132e3-113">Retrieving Status Information</span></span>

<span data-ttu-id="132e3-114">Status Informationen werden mithilfe des Zeit Gebers aktualisiert, der in der **Init** -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="132e3-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="132e3-115">Der gesamte Status wird mit demselben Zeitgeber aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="132e3-115">All status is updated using the same timer.</span></span> <span data-ttu-id="132e3-116">Der Name der Funktion für das Timer-Ereignis ist **OnTimer**.</span><span class="sxs-lookup"><span data-stu-id="132e3-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="132e3-117">**OnTimer** bestimmt die Informationen, die auf der Grundlage der Benutzer Auswahl angezeigt werden, die in der globalen Variablen "g \_ ocurrentdlitem" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="132e3-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="132e3-118">Die-Funktion testet zunächst, ob die Größe oder die Fortschritts Werte gültig sind, und erstellt für jeden Fall eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="132e3-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="132e3-119">Wenn ein Wert gültig ist, stellt die Zeichenfolge die Byte Anzahl dar.</span><span class="sxs-lookup"><span data-stu-id="132e3-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="132e3-120">Wenn der Wert nicht gültig ist, z. b.-1, stellt die Zeichenfolge eine Meldung bereit, um den Benutzer darüber zu informieren, dass die Informationen noch nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="132e3-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="132e3-121">**Als Nächstes bestimmt ein** switchblock, ob der Download für das ausgewählte Element abgeschlossen oder abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="132e3-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="132e3-122">Wenn einer der Fälle true ist, wird der Wert der Variablen Größe oder des Fortschritts entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="132e3-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="132e3-123">Schließlich werden die Statusinformationen im div-Element mit dem Namen "dlstate" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="132e3-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="132e3-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="132e3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="132e3-125">**Verwenden des Download-Managers**</span><span class="sxs-lookup"><span data-stu-id="132e3-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




