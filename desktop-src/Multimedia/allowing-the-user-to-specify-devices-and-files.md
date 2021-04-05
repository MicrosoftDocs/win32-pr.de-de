---
title: Zulassen der Angabe von Geräten und Dateien durch den Benutzer
description: Zulassen der Angabe von Geräten und Dateien durch den Benutzer
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Mciwndopendialog-Makro
- Mciwndopen-Makro
- Mciwndopeninterface-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710985"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="c4f2b-106">Zulassen der Angabe von Geräten und Dateien durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="c4f2b-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="c4f2b-107">Mithilfe der Makros [**mciwndopendialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)und [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) und der [**getopenfileamepreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) -Funktion können Sie ein Gerät oder eine Datei mit einem vorhandenen mciwnd-Fenster verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="c4f2b-108">Verwenden Sie **mciwndopendialog**, damit ein Benutzer Ihrer Anwendung eine wieder zugebende Datei auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="c4f2b-109">Dieses Makro zeigt das Dialogfeld **Öffnen** (im folgenden Screenshot gezeigt) zum Auswählen einer Datei an und ordnet die ausgewählte Datei dem aktuellen mciwnd-Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![Bild des mciwnd-Fensters](images/mciwnd3.gif)

<span data-ttu-id="c4f2b-111">Sie können einem Benutzer Ihrer Anwendung gestatten, eine Datei auszuwählen, die einem mciwnd-Fenster zugeordnet werden soll, und die Datei mithilfe von [**getopenfileamepreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) und [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)in einer Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="c4f2b-112">Die Funktion **getopenfileamepreview** zeigt das Dialogfeld **Öffnen** zum Auswählen einer Datei an und ermöglicht dem Benutzer, seinen Inhalt anzuzeigen (wiederzugeben).</span><span class="sxs-lookup"><span data-stu-id="c4f2b-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="c4f2b-113">Wenn der Name einer vorhandenen Datei im Dialogfeld angegeben wird, stellt **getopenfileamepreview** ein kleines Steuerelement bereit, damit der Benutzer den Inhalt der Datei in der Vorschau anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="c4f2b-114">Mithilfe von **mciwndopen** können Sie eine angegebene, mit **getopenfileamepreview** ausgewählte oder auf andere Weise angegebene Datei mit einem mciwnd-Fenster verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="c4f2b-115">Sie können auch **mciwndopen** verwenden, um ein Gerät anzugeben, das einem mciwnd-Fenster zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="c4f2b-116">Beispielsweise können Sie einen Gerätenamen verwenden, z. b. "CDAudio".</span><span class="sxs-lookup"><span data-stu-id="c4f2b-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="c4f2b-117">Verwenden Sie das [**mciwndopeninterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) -Makro, um Multimediadaten ein mciwnd-Fenster mit einer Datei Schnittstelle oder einer Datenstrom Schnittstelle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="c4f2b-118">Weitere Informationen zu Datei-und Datenstrom Schnittstellen finden Sie unter [avifile-Funktionen und-Makros](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="c4f2b-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="c4f2b-119">Vor dem Zuordnen einer neuen Datei oder eines Geräts zu einem mciwnd-Fenster schließen [**mciwndopendialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) und [**mciwndopen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) alle Geräte, die derzeit dem Fenster zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="c4f2b-120">Die Anwendung muss keine geöffneten Geräte schließen, bevor Sie diese Makros verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c4f2b-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




