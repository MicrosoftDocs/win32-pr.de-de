---
description: Ermitteln der Fehlerquelle
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Ermitteln der Fehlerquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041503"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="df58f-103">Ermitteln der Fehlerquelle</span><span class="sxs-lookup"><span data-stu-id="df58f-103">Finding the Source of an Error</span></span>

<span data-ttu-id="df58f-104">Mithilfe von com+ und anderen Tools können Sie die Quelle diagnostizieren und eine Beschreibung der Anwendungsfehler abrufen.</span><span class="sxs-lookup"><span data-stu-id="df58f-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="df58f-105">Wenn Sie feststellen, dass der Anwendungsfehler durch com+ verursacht wird, können Sie die Fehlermeldung mit der Datei "Winerror. h" oder mithilfe des Microsoft Visual C++ Fehler-Hilfsprogramms interpretieren.</span><span class="sxs-lookup"><span data-stu-id="df58f-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="df58f-106">Wenn die Serveranwendung ausfällt oder unerwartetes Verhalten verursacht, müssen Sie zuerst bestimmen, wo der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="df58f-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="df58f-107">Das System Ereignisanzeige nachverfolgt Anwendungs-, Sicherheits-und Systemereignisse.</span><span class="sxs-lookup"><span data-stu-id="df58f-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="df58f-108">Viele "Stille" Fehler werden hier aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="df58f-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="df58f-109">Allerdings werden nicht alle Fehler in der Ereignisanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df58f-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="df58f-110">Zuerst sollten Sie auf das Anwendungsprotokoll in der Ereignisanzeige verweisen, um die Anwendung zu überprüfen, die der Ereignismeldung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="df58f-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="df58f-111">(Da Sie auch Ereignisprotokolle archivieren können, können Sie einen Ereignis Verlauf des Fehlers nachverfolgen.) Wenn Sie in Ihrem Protokoll auf einen Eintrag doppelklicken, wird eine Seite mit **Ereignis Eigenschaften** aktiviert, die weitere Informationen über das System Ereignis bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="df58f-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="df58f-112">Weitere Informationen zum Debuggen einer COM+-Anwendung finden Sie unter [Debuggen von com+-Anwendungen](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="df58f-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df58f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df58f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df58f-114">Fehler Isolation und FailFast-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="df58f-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="df58f-115">Ändern der Rückgabewerte durch com+</span><span class="sxs-lookup"><span data-stu-id="df58f-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="df58f-116">Interpretieren von Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="df58f-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="df58f-117">Strategien für die Behandlung von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="df58f-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="df58f-118">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="df58f-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



