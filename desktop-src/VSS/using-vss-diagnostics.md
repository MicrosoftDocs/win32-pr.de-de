---
description: Vsdiagview und vssagent sind Tools, die Sie verwenden können, um Probleme mit VSS-Anwendungen zu beheben. Beachten Sie, dass diese Tools im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten sind.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Verwenden der VSS-Diagnose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343683"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="758a0-103">Verwenden der VSS-Diagnose</span><span class="sxs-lookup"><span data-stu-id="758a0-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="758a0-104">Vsdiagview und vssagent sind Tools, die Sie verwenden können, um Probleme mit VSS-Anwendungen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="758a0-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="758a0-105">Diese Tools sind im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="758a0-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="758a0-106">Sie können die Windows SDK von herunterladen [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="758a0-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="758a0-107">In der Windows SDK-Installation finden Sie diese Tools in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).</span><span class="sxs-lookup"><span data-stu-id="758a0-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="758a0-108">Sammeln von Daten</span><span class="sxs-lookup"><span data-stu-id="758a0-108">Gathering Data</span></span>

<span data-ttu-id="758a0-109">Sie können Daten mit dem Befehl vssagent sammeln.</span><span class="sxs-lookup"><span data-stu-id="758a0-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="758a0-110">**So erfassen Sie Daten mithilfe von vssagent**</span><span class="sxs-lookup"><span data-stu-id="758a0-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="758a0-111">Verwenden Sie zum Erfassen von Daten über die Befehlszeile den vssagent-Befehl wie folgt:</span><span class="sxs-lookup"><span data-stu-id="758a0-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="758a0-112">**vssagent-** " *xmlFileName \* \* *. XML* " erfassen*</span><span class="sxs-lookup"><span data-stu-id="758a0-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="758a0-113">Informationen zum Anzeigen der Ausgabedatei finden Sie im folgenden Abschnitt zum Anzeigen von Daten.</span><span class="sxs-lookup"><span data-stu-id="758a0-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="758a0-114">Anzeigen von Daten</span><span class="sxs-lookup"><span data-stu-id="758a0-114">Viewing Data</span></span>

<span data-ttu-id="758a0-115">Die vsdiagview-Anwendung kann verwendet werden, um Daten anzuzeigen, die mit dem vssagent-Befehl erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="758a0-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="758a0-116">Vsdiagview zeigt die folgenden Informationen zum Computer an:</span><span class="sxs-lookup"><span data-stu-id="758a0-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="758a0-117">Informationen zum Computer, z. b. Betriebssystemversion, gesamter Arbeitsspeicher und CPU-Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="758a0-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="758a0-118">Die Namen und Versionsnummern der VSS-Binärdateien</span><span class="sxs-lookup"><span data-stu-id="758a0-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="758a0-119">Die Namen und Eigenschaften der Datenträger-und Volumegeräte</span><span class="sxs-lookup"><span data-stu-id="758a0-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="758a0-120">Die Namen und Eigenschaften der com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="758a0-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="758a0-121">Die Namen der Ereignisprotokolle, die für die Diagnose von VSS-Problemen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="758a0-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="758a0-122">Die Namen aller VSS-Writer und der Ereignisse, die Sie behandeln</span><span class="sxs-lookup"><span data-stu-id="758a0-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="758a0-123">Informationen zu anderen Betriebssystemdateien</span><span class="sxs-lookup"><span data-stu-id="758a0-123">Information about other operating system files</span></span>

<span data-ttu-id="758a0-124">**So zeigen Sie Daten mithilfe von vsdiagview an**</span><span class="sxs-lookup"><span data-stu-id="758a0-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="758a0-125">Wählen Sie im Menü Datei die Option **Öffnen** aus, um nach einer Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="758a0-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="758a0-126">(Der Standard Speicherort ist C: \\ vssdiag.)</span><span class="sxs-lookup"><span data-stu-id="758a0-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="758a0-127">Klicken Sie auf **Öffnen** , um die Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="758a0-127">Click **Open** to view the data.</span></span>

 

 



