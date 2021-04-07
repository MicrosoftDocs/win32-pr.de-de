---
description: Manuelle Konvertierung von MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Manuelle Konvertierung von MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748297"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="1e815-103">Manuelle Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="1e815-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="1e815-104">Möglicherweise möchten Sie die Konvertierung von MTS-Paketen in com+-Anwendungen isolieren, sodass diese außerhalb des Windows-Setup Vorgangs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e815-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="1e815-105">Das folgende Verfahren bietet einen alternativen Ansatz:</span><span class="sxs-lookup"><span data-stu-id="1e815-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="1e815-106">Exportieren Sie die MTS-Pakete mit dem Paket Export Feature "MTS 2,0" (was zu einer MTS-Paketdatei und einer Sammlung anderer Dateien führt).</span><span class="sxs-lookup"><span data-stu-id="1e815-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="1e815-107">Löschen Sie die MTS-Pakete und die upgradefenster, oder führen Sie eine Neuinstallation von Windows aus.</span><span class="sxs-lookup"><span data-stu-id="1e815-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="1e815-108">Installieren Sie die MTS-Paketdateien (. Pak) auf einem System unter Windows 2000 oder höher, indem Sie den Anwendungsinstallations-Assistenten des Verwaltungs Tools des Komponenten Diensts verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e815-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="1e815-109">Außerdem müssen Sie die "Run as"-Identität der Anwendung in der Systemregistrierung unter **HKEY \_ Local Machine Machines \_ " \\ \\ \\ AppID \\ runas**" zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="1e815-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="1e815-110">Nur bei der automatischen Konvertierung (über Windows Setup oder durch Ausführen des Dienstprogramms mtstocom) wird die mtstocom-Protokolldatei generiert.</span><span class="sxs-lookup"><span data-stu-id="1e815-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="1e815-111">Diese Datei wird nicht generiert, wenn die manuelle Konvertierung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e815-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e815-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e815-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e815-113">Automatische Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="1e815-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="1e815-114">Ergebnisse und Probleme bei der com+-Konvertierung</span><span class="sxs-lookup"><span data-stu-id="1e815-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="1e815-115">MTS-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e815-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



