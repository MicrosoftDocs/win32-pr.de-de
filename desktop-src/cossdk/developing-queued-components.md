---
description: Entwickeln von Komponenten in der Warteschlange
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Entwickeln von Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748041"
---
# <a name="developing-queued-components"></a><span data-ttu-id="44a51-103">Entwickeln von Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="44a51-103">Developing Queued Components</span></span>

<span data-ttu-id="44a51-104">Der in der Warteschlange befindliche Komponenten Dienst erfordert, dass alle Anwendungsmethoden nur \[ in \] Parameter ohne Rückgabewerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="44a51-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="44a51-105">Da das Server Objekt nicht notwendigerweise verfügbar ist, wenn der Client den-Befehl ausführt, können Server Ergebnisse zurückgegeben werden, indem eine Nachricht gesendet wird, die ein anderes-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="44a51-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="44a51-106">Auf diese Weise erfolgt die bidirektionale Kommunikation nicht in jedem Fall, sondern nur, wenn dies erforderlich ist, durch eine Reihe von unidirektionalen Nachrichten zwischen Objekten.</span><span class="sxs-lookup"><span data-stu-id="44a51-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="44a51-107">Wenn Sie den com+-Dienst in der Warteschlange verwenden möchten, müssen Sie den [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) -Dienst bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="44a51-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="44a51-108">Message Queuing wird nicht automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="44a51-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="44a51-109">Message Queuing müssen während der Einrichtung des Betriebssystems **oder mithilfe der** Option "Software" ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="44a51-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="44a51-110">Ein internes Message Queuing Zertifikat wird bei der Anmeldung automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="44a51-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="44a51-111">Die in der folgenden Tabelle beschriebenen Themen enthalten weitere Überlegungen zu spezielleren Situationen.</span><span class="sxs-lookup"><span data-stu-id="44a51-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="44a51-112">Thema</span><span class="sxs-lookup"><span data-stu-id="44a51-112">Topic</span></span>                                                                                           | <span data-ttu-id="44a51-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44a51-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a51-114">[Übergeben von Objekten als Parameter](passing-objects-as-parameters.md)s</span><span class="sxs-lookup"><span data-stu-id="44a51-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="44a51-115">Beschreibt, wie-Objekte als \[ \] Parameter an in die Warteschlange eingereihte Komponenten übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="44a51-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="44a51-116">Sicherheitseinschränkungen im Arbeitsgruppen Modus</span><span class="sxs-lookup"><span data-stu-id="44a51-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="44a51-117">Beschreibt Einschränkungen bei der Verwendung von Message Queuing Authentifizierung im Arbeitsgruppen Modus.</span><span class="sxs-lookup"><span data-stu-id="44a51-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="44a51-118">Überlegungen zum Threading</span><span class="sxs-lookup"><span data-stu-id="44a51-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="44a51-119">Beschreibt bestimmte Probleme im Zusammenhang mit der Übergabe von Aufzeichnungs Schnittstellen Zeigern zwischen Threads.</span><span class="sxs-lookup"><span data-stu-id="44a51-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="44a51-120">Empfangen einer Antwort</span><span class="sxs-lookup"><span data-stu-id="44a51-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="44a51-121">Beschreibt das Erstellen einer Antwort auf einen in der Warteschlange befindlichen Komponenten Aufruf.</span><span class="sxs-lookup"><span data-stu-id="44a51-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




