---
description: Apps können die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um die APP vom Druckertreiber zu isolieren und die Zuverlässigkeit der apps zu verbessern.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Gewusst wie: Verwenden der Anwendungs Isolation'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215965"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="37c05-103">Gewusst wie: Verwenden der Anwendungs Isolation</span><span class="sxs-lookup"><span data-stu-id="37c05-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="37c05-104">Apps können die Druckertreiber Isolation in Ihrem App-Manifest deklarieren, um die APP vom Druckertreiber zu isolieren und die Zuverlässigkeit der APP zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="37c05-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="37c05-105">Der Windows-Druckdienst ermöglicht die Ausführung von Druckertreibern in Prozessen, die von dem Prozess getrennt sind, in dem der Druck Spooler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37c05-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="37c05-106">Wenn Sie diese Funktion verwenden, verhindert Ihre APP, dass Sie abstürzt, wenn der Druckertreiber einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="37c05-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="37c05-107">Die Druckertreiber Isolation ist in Windows 7 und Windows Server 2008 R2 implementiert.</span><span class="sxs-lookup"><span data-stu-id="37c05-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="37c05-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="37c05-108">Prerequisites</span></span>

-   <span data-ttu-id="37c05-109">Eine verwaltete Code-oder Windows Store-App, die die Druckfunktion von Windows verwendet.</span><span class="sxs-lookup"><span data-stu-id="37c05-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="37c05-110">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="37c05-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="37c05-111">Aktualisieren des App-Manifests</span><span class="sxs-lookup"><span data-stu-id="37c05-111">Update the app manifest</span></span>

<span data-ttu-id="37c05-112">Wenn Sie die Druckertreiber Isolation aktivieren, müssen Sie das **printerdriverisolation** -Element dem App-Manifest hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37c05-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="37c05-113">Gehen Sie dazu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="37c05-113">Here's how:</span></span>

1.  <span data-ttu-id="37c05-114">Bearbeiten Sie das App-Manifest, und fügen Sie das **printerdriverisolation** -Element mit dem Wert **true** zum **Windows Settings** -Element des **Application** -Elements hinzu, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="37c05-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="37c05-115">Erstellen Sie die APP neu.</span><span class="sxs-lookup"><span data-stu-id="37c05-115">Rebuild your app.</span></span>

 

 



