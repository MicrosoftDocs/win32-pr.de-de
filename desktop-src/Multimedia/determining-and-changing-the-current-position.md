---
title: Bestimmen und Ändern der aktuellen Position
description: Bestimmen und Ändern der aktuellen Position
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Mciwndgetstart-Makro
- Mciwndgetend-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471397"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="ff343-105">Bestimmen und Ändern der aktuellen Position</span><span class="sxs-lookup"><span data-stu-id="ff343-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="ff343-106">Wenn eine Datei oder ein Gerät einem mciwnd-Fenster zugeordnet ist, wird die Wiedergabe Position anfangs unabhängig vom Medientyp am Anfang des Inhalts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ff343-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="ff343-107">Während der Wiedergabe wird die Wiedergabe Position linear durch den Inhalt verschoben, und wenn die Wiedergabe ununterbrochen erfolgt, erreicht schließlich das Ende des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="ff343-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="ff343-108">Wenn eine Unterbrechung auftritt, ist die aktuelle Wiedergabe Position der Speicherort, an dem die Wiedergabe beendet oder angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="ff343-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="ff343-109">Sie können die Speicherorte für den Anfang und das Ende des Inhalts abrufen, indem Sie die Makros [**mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) und [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="ff343-110">Sie können die Länge des Inhalts ermitteln, indem Sie den von **mciwndgetstart** zurückgegebenen Wert von dem Wert subtrahieren, der von **mciwndgetend** zurückgegeben wurde, oder indem Sie das [**mciwndgetlength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="ff343-111">Sie können die aktuelle Wiedergabe Position abrufen, indem Sie das [**mciwndgetposition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) -Makro verwenden, oder Sie können die Wiedergabe Position als NULL-terminierte Zeichenfolge abrufen, indem Sie das [**mciwndgetpositionstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="ff343-112">Verwenden Sie zum Ändern der aktuellen Wiedergabe Position die Makros [**mciwndhome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**mciwndend**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)und [**mciwndseek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="ff343-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="ff343-113">Sie können die Wiedergabe Position an den Anfang des Inhalts verschieben, indem Sie **mciwndhome** oder das Ende des Inhalts mit **mciwndend** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="ff343-114">Verwenden Sie **mciwndseek** , um die Wiedergabe Position an eine beliebige Position im Inhalt zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ff343-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="ff343-115">Sie können den Inhalt auch durchlaufen, indem Sie das [**mciwndstep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="ff343-116">Beginnend mit der aktuellen Wiedergabe Position verschiebt dieses Makro die Wiedergabe Position um ein angegebenes Inkrement vorwärts oder rückwärts.</span><span class="sxs-lookup"><span data-stu-id="ff343-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="ff343-117">Die Einheiten, die zum Angeben der Position verwendet werden, variieren je nach Medientypen und-Geräten.</span><span class="sxs-lookup"><span data-stu-id="ff343-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="ff343-118">Die Wiedergabe Position für vom MCIAVI-Gerät verwendete AVI-Dateien wird z. b. in Frames gemessen. die Wiedergabe Position für CD-Audiodateien, Wellenform-Audiodateien und MIDI-Dateien wird in Millisekunden gemessen.</span><span class="sxs-lookup"><span data-stu-id="ff343-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="ff343-119">Geräte für andere Medientypen und Geräte von Drittanbietern können andere Einheiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff343-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="ff343-120">Informationen zum Ermitteln dieser Einheiten finden Sie unter [Wiedergabe Erweiterungen](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="ff343-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




