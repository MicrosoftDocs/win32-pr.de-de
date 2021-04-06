---
title: Software Verteilung
description: Software Verteilung
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media-Format-SDK, Software Verteilung
- Advanced Systems Format (ASF), Software Verteilung
- ASF (Advanced Systems Format), Software Verteilung
- SDK für Windows Media-Format, Neuverteilung
- Advanced Systems Format (ASF), Verteilung
- ASF (Advanced Systems Format), Verteilung
- Software Verteilung, Informationen zu
- Weiterverteilung, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709474"
---
# <a name="software-redistribution"></a><span data-ttu-id="d4b7a-111">Software Verteilung</span><span class="sxs-lookup"><span data-stu-id="d4b7a-111">Software Redistribution</span></span>

<span data-ttu-id="d4b7a-112">Die Einbindung von Software im Windows Media-Format in eine Anwendungs Einrichtung wird als Neuverteilung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="d4b7a-113">Das Windows Media-Format SDK enthält ein Installationspaket, das in das Anwendungs Setup aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="d4b7a-114">Das Installationspaket ist eine ausführbare Datei mit dem Namen wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="d4b7a-115">Wenn Sie das Windows Media-Format-SDK installieren, wird das Installationspaket in den \\ Ordner "Redist" des Installationsverzeichnisses ( \\ standardmäßig "c: wmsdk \\ wmfsdk") kopiert.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="d4b7a-116">In den folgenden Abschnitten finden Sie Prozeduren und weitere Informationen zum Setup für die Software Verteilung.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="d4b7a-117">`Section`</span><span class="sxs-lookup"><span data-stu-id="d4b7a-117">Section</span></span>                                                                            | <span data-ttu-id="d4b7a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4b7a-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4b7a-119">So erstellen Sie eine weitergabeeinrichtung</span><span class="sxs-lookup"><span data-stu-id="d4b7a-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="d4b7a-120">Beschreibt das Verfahren zum Erstellen eines Anwendungs Setups.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="d4b7a-121">Ermitteln des Setup Status</span><span class="sxs-lookup"><span data-stu-id="d4b7a-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="d4b7a-122">Stellt Beispielcode bereit, mit dem die Registrierung auf den Installationsstatus überprüft wird, um zu bestimmen, ob das Verteilungs Paket installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="d4b7a-123">Beispiel Code für die weitergabeeinrichtung</span><span class="sxs-lookup"><span data-stu-id="d4b7a-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="d4b7a-124">Bietet Beispielcode, der in der Setup Routine verwendet werden kann, um die weitergabepakete im stillen Modus auszuführen und die Setup Routine zu benachrichtigen, wenn der Computer neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d4b7a-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4b7a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4b7a-126">**Überlegungen zu Projekten**</span><span class="sxs-lookup"><span data-stu-id="d4b7a-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




