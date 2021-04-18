---
title: Multimedia-Aufzeichnung
description: Multimedia-Aufzeichnung
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Mciwndcreate-Funktion
- Mciwndnew-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388276"
---
# <a name="multimedia-recording"></a><span data-ttu-id="a79a4-105">Multimedia-Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="a79a4-105">Multimedia Recording</span></span>

<span data-ttu-id="a79a4-106">Sie können Aufzeichnungsfunktionen in Ihrer Anwendung implementieren, indem Sie die in mciwnd integrierte Benutzeroberfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="a79a4-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="a79a4-107">Sie können die [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion und das [**mciwndnew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) -Makro verwenden, um Steuerelemente zum Starten und Beenden der Aufzeichnung und zum Speichern der aufgezeichneten Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a79a4-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="a79a4-108">Mithilfe von " **mciwndcreate**" können Sie Fenster Stile zum Anzeigen eines mciwnd-Fensters und zum Einschließen der Schaltfläche **Datensatz** auf der Symbolleiste angeben.</span><span class="sxs-lookup"><span data-stu-id="a79a4-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="a79a4-109">Mit **mciwndnew** können Sie den Gerätetyp angeben, der aufgezeichnet wird, und angeben, dass die Informationen in einer neuen Datei erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a79a4-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="a79a4-110">Wenn Ihre Anwendung eine höhere Komplexität erfordert, können Sie die Aufzeichnung automatisieren und anpassen, indem Sie das [**mciwndrecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="a79a4-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="a79a4-111">Weitere Informationen finden Sie unter [Anpassen des Aufzeichnungsprozesses](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="a79a4-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="a79a4-112">Einige Geräte, z. b. CD-Audiodaten und MCIAVI, werden nur für die Wiedergabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="a79a4-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="a79a4-113">Andere Geräte, z. b. Waveform-Audiogeräte, können für die Aufzeichnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a79a4-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="a79a4-114">Wenn Sie ein Gerät angeben, das nicht aufzeichnen kann, lässt mciwnd die Schaltfläche **Datensatz** von der Symbolleiste aus.</span><span class="sxs-lookup"><span data-stu-id="a79a4-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




