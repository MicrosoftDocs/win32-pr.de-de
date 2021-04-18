---
description: Client-Side Fehler
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344948"
---
# <a name="client-side-errors"></a><span data-ttu-id="437a4-103">Client-Side Fehler</span><span class="sxs-lookup"><span data-stu-id="437a4-103">Client-Side Errors</span></span>

<span data-ttu-id="437a4-104">Client seitige Fehler werden ähnlich wie serverseitige Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="437a4-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="437a4-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) können eine Nachricht in die Ziel Warteschlange verschieben, wenn Sie z. b. nicht vom Client zum Server verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="437a4-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="437a4-106">In diesem Fall wird die Nachricht in die Client seitige Warteschlange für unzustellbare Nachrichten verschoben.</span><span class="sxs-lookup"><span data-stu-id="437a4-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="437a4-107">Der Dienst "com+-Warteschlangen Komponenten" überwacht die Warteschlange für unzustellbare Meldungen</span><span class="sxs-lookup"><span data-stu-id="437a4-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="437a4-108">Wenn Nachrichten verschoben wurden, erstellt der in der Warteschlange befindliche Komponenten Dienst eine Instanz der Ausnahme Klasse und ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)anzufordern.</span><span class="sxs-lookup"><span data-stu-id="437a4-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="437a4-109">Wenn dies erfolgreich ist, ruft der Monitor für die Warteschlange für unzustellbare Nachrichten [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)auf.</span><span class="sxs-lookup"><span data-stu-id="437a4-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="437a4-110">Das-Objekt kann einige Maßnahmen ergreifen, um die Auswirkungen einer vorherigen Transaktion umzukehren.</span><span class="sxs-lookup"><span data-stu-id="437a4-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="437a4-111">Wenn bei der Wiedergabe ein Commit ausgeführt wird, wird die Nachricht aus der Warteschlange für unzustellbare Nachrichten des</span><span class="sxs-lookup"><span data-stu-id="437a4-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="437a4-112">Wenn die Wiedergabe fehlschlägt oder die erforderliche CLSID und Schnittstelle nicht verfügbar sind, verbleibt die Nachricht in der Warteschlange für unzustellbare Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="437a4-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="437a4-113">Wenn Sie in den oben beschriebenen Prozess eingreifen müssen oder eine nicht verarbeitbare Nachricht aus der letzten ruhenden Warteschlange verschieben müssen, verwenden Sie das Hilfsprogramm Nachrichten Verschiebung.</span><span class="sxs-lookup"><span data-stu-id="437a4-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="437a4-114">Weitere Informationen zum Hilfsprogramm für den Nachrichten Verschiebungsvorgang finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="437a4-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="437a4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="437a4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="437a4-116">Persistente Client-Side Fehler</span><span class="sxs-lookup"><span data-stu-id="437a4-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="437a4-117">Server seitige Fehler</span><span class="sxs-lookup"><span data-stu-id="437a4-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
