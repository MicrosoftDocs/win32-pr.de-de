---
description: Problembehandlung
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338911"
---
# <a name="troubleshooting"></a><span data-ttu-id="af452-103">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="af452-103">Troubleshooting</span></span>

<span data-ttu-id="af452-104">Wenn Sie Probleme mit der Diagnose ihrer Anwendungsfehler haben, lesen Sie die folgenden Tipps zur Problembehandlung:</span><span class="sxs-lookup"><span data-stu-id="af452-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="af452-105">Stellen Sie sicher, dass die Distributed Transaction Coordinator (DTC) auf allen Servern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af452-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="af452-106">Überprüfen Sie die Netzwerkkommunikation, indem Sie zunächst auf einem lokalen Computer testen, ob die Anwendung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="af452-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="af452-107">Wenn Sie TCP/IP im Netzwerk ausführen, können Sie mit dem ping.exe-Hilfsprogramm überprüfen, ob sich die Computer im Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="af452-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="af452-108">Stellen Sie sicher, dass sich SQL und DTC auf demselben Computer befinden oder dass das DTC-Client Konfigurationsprogramm angibt, dass sich der DTC auf einem anderen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="af452-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="af452-109">Wenn dies nicht der Fall ist, gibt SQLCONNECT intern einen Fehler zurück, wenn er von einer Transaktions Komponente aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="af452-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="af452-110">Legen Sie den Timeout Wert für die Transaktion auf eine höhere Zahl als die Standard-60 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="af452-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="af452-111">Nachdem das Transaktions Timeout abgelaufen ist, bricht com+ die Transaktion ab.</span><span class="sxs-lookup"><span data-stu-id="af452-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="af452-112">Alle nachfolgenden Aufrufe der Komponente kehren sofort zurück, wobei der Kontext \_ E \_ abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="af452-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="af452-113">Stellen Sie sicher, dass die ODBC-Treiber Thread sicher sind und nicht über Thread Affinität verfügen.</span><span class="sxs-lookup"><span data-stu-id="af452-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="af452-114">Wenn Sie Schwierigkeiten haben, eine Anwendung auf mehrere Server zu überarbeiten, starten Sie den Client neu, und überprüfen Sie dann, ob der Domänen Controller ordnungsgemäß konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="af452-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af452-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af452-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af452-116">Fehler Isolation und FailFast-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="af452-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="af452-117">Ermitteln der Fehlerquelle</span><span class="sxs-lookup"><span data-stu-id="af452-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="af452-118">Ändern der Rückgabewerte durch com+</span><span class="sxs-lookup"><span data-stu-id="af452-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="af452-119">Interpretieren von Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="af452-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="af452-120">Strategien für die Behandlung von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="af452-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



