---
title: Speichern erfasster Daten in einer neuen Datei
description: Speichern erfasster Daten in einer neuen Datei
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS Meldung
- capfilesaveas-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710451"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="9171f-105">Speichern erfasster Daten in einer neuen Datei</span><span class="sxs-lookup"><span data-stu-id="9171f-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="9171f-106">Wenn der Benutzer erfasste Daten speichern möchte, sollte die Anwendung den Inhalt der Erfassungs Datei in einer anderen Datei speichern, indem [**die \_ \_ Datei " \_ SaveAs**](wm-cap-file-saveas.md) " der WM-Cap-Datei (oder das Makro " [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ") verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9171f-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="9171f-107">Diese Meldung ändert nicht den Namen oder den Inhalt der Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="9171f-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="9171f-108">Die Anwendung muss einen Namen für die neue Datei angeben, da die Erfassungs Datei den ursprünglichen Dateinamen beibehält.</span><span class="sxs-lookup"><span data-stu-id="9171f-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="9171f-109">In der Regel wird eine Erfassungs Datei für das größte erwartete Erfassungs Segment reserviert, und es kann nur ein Teil davon zum Erfassen von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9171f-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="9171f-110">In dieser Meldung wird nur der Teil der Erfassungs Datei kopiert, der die Aufzeichnungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="9171f-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




