---
title: Speichern von aufgezeichneten Inhalten
description: Speichern von aufgezeichneten Inhalten
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Mciwndsave-Makro
- Mciwndsavedialog-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710446"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="8b167-105">Speichern von aufgezeichneten Inhalten</span><span class="sxs-lookup"><span data-stu-id="8b167-105">Saving Recorded Content</span></span>

<span data-ttu-id="8b167-106">Nachdem Sie die Aufzeichnung abgeschlossen haben, können Sie den Inhalt mithilfe des Makros [**mciwndsave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) oder [**mciwndsavedialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) oder mithilfe der [**getsavefile Name Preview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) -Funktion mit **mciwndsave** speichern.</span><span class="sxs-lookup"><span data-stu-id="8b167-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="8b167-107">Das **mciwndsave** -Makro speichert Daten in der Datei, die dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8b167-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="8b167-108">Das **mciwndsavedialog** -Makro ermöglicht dem Benutzer das Angeben eines Datei namens und das Speichern der aufgezeichneten Daten in der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="8b167-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="8b167-109">Die Funktion " **getsavefileamepreview** " zeigt das Dialogfeld " **SaveAs** " zum Auswählen einer Datei an und ermöglicht dem Benutzer die Vorschau der Datei.</span><span class="sxs-lookup"><span data-stu-id="8b167-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="8b167-110">Wenn der Name einer vorhandenen Datei im Dialogfeld " **SaveAs** " angegeben wird, stellt **getsavefileamepreview** ein kleines Steuerelement im Dialogfeld bereit, damit der Benutzer den Inhalt der Datei in der Vorschau anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="8b167-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="8b167-111">Sie können die aufgezeichneten Daten in einer Datei speichern, die mit " **getsavefileamepreview** " mithilfe von " **mciwndsave**" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b167-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




