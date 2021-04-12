---
title: So erstellen Sie eine weitergabeeinrichtung
description: So erstellen Sie eine weitergabeeinrichtung
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media-Format-SDK, Software Verteilung
- Advanced Systems Format (ASF), Software Verteilung
- ASF (Advanced Systems Format), Software Verteilung
- SDK für Windows Media-Format, Neuverteilung
- Advanced Systems Format (ASF), Verteilung
- ASF (Advanced Systems Format), Verteilung
- Software Verteilung, erstellen
- Software Verteilung, WMFDist.exe
- Verteilung, erstellen
- Neuverteilung, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206689"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="d359c-114">So erstellen Sie eine weitergabeeinrichtung</span><span class="sxs-lookup"><span data-stu-id="d359c-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="d359c-115">Lassen Sie Ihre Anwendungs Dateien von der Setup Routine installieren, und nehmen Sie vor dem Aufrufen des Verteilungs Pakets die erforderlichen Einstellungen vor.</span><span class="sxs-lookup"><span data-stu-id="d359c-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="d359c-116">Installieren Sie WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="d359c-116">Install WMFDist.exe.</span></span> <span data-ttu-id="d359c-117">Sie können das Flag "/Q: a" verwenden, um eine unbeaufsichtigte Installation durchzuführen und die Benutzeroberfläche der weitergabeeinrichtung während der Installation der Anwendung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="d359c-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="d359c-118">Ihre Routine muss dann erkennen, ob ein Neustart am Ende erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d359c-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="d359c-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d359c-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="d359c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d359c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d359c-121">**Software Verteilung**</span><span class="sxs-lookup"><span data-stu-id="d359c-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




