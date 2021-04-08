---
description: Der \_ msiexecute Mutex wird nur beim Verarbeiten der InstallExecuteSequence-Tabelle, der AdminExecuteSequence-Tabelle oder der AdvtExecuteSequence-Tabelle festgelegt.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864555"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="5b4f1-103">\_Msiexecute Mutex</span><span class="sxs-lookup"><span data-stu-id="5b4f1-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="5b4f1-104">Der \_ msiexecute Mutex wird nur beim Verarbeiten der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md), der [AdminExecuteSequence](adminexecutesequence-table.md)-Tabelle oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="5b4f1-105">Da zwei Installationen nicht im selben Prozess ausgeführt werden können, wird beim Versuch, die API (Application Programming Interface) des Installers aufzurufen, die Fehler Installation, die \_ \_ bereits \_ ausgeführt wird (1618), in zwei Fällen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="5b4f1-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="5b4f1-106">Während der \_ msiexecute-Mutex festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="5b4f1-107">Während der aktuelle Prozess die Tabelle " [InstallUISequence](installuisequence-table.md) " oder die [Tabelle "AdminUISequence](adminuisequence-table.md)" verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="5b4f1-108">Informationen zu den installierten Anwendungen finden Sie in den [Ereignis Protokollierungs](event-logging.md) Meldungen.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="5b4f1-109">In Fällen, in denen es nicht praktikabel ist, eine Fehlermeldung zu einer bereits aktiven Fehlermeldung zurückzugeben \_ \_ \_ , können Sie den aktuellen Status des Windows Installer Dienstanbieter abrufen, bevor Sie versuchen, die Installation mit der Funktion [**queryservicestatusex**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zu starten.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="5b4f1-110">Der Windows Installer-Dienst wird zurzeit ausgeführt, wenn der Wert des **dwcontrolsaccepted** -Members der zurückgegebenen [**Dienst \_ Status- \_ Prozess**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) Struktur " **Service \_ Accept \_ Shutdown**" lautet.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="5b4f1-111">**Windows Installer 2,0:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="5b4f1-112">Die Verwendung der Funktion [**queryservicestatusex**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) zum Abrufen des aktuellen Status der Windows Installer Dienstanbieter erfordert Windows Installer Version 3,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5b4f1-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 
