---
description: Konzepte der com+-Warteschlangen
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Konzepte der com+-Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341124"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="50d15-103">Konzepte der com+-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="50d15-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="50d15-104">Basierend auf [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Diensten bietet der in der Warteschlange befindliche Komponenten Dienst eine einfache Möglichkeit zum asynchronen Aufrufen und Ausführen von-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="50d15-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="50d15-105">Die Verarbeitung kann ohne Rücksicht auf die Verfügbarkeit oder den Zugriff des Absenders oder des Empfängers erfolgen.</span><span class="sxs-lookup"><span data-stu-id="50d15-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="50d15-106">In com-begriffen ist eine *Warteschlange* ein Speicherbereich, der Nachrichten für den späteren Abruf speichert.</span><span class="sxs-lookup"><span data-stu-id="50d15-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="50d15-107">Queueing bietet einen Mechanismus für die verbindungslose Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="50d15-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="50d15-108">Das heißt, dass der Absender und der Empfänger nicht direkt verbunden sind und nur über Warteschlangen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="50d15-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="50d15-109">Warteschlangen bieten eine Möglichkeit, die Informationen zu speichern, bis der Empfänger zum Abrufen bereit ist.</span><span class="sxs-lookup"><span data-stu-id="50d15-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="50d15-110">Der Absender und der Empfänger kommunizieren indirekt, sodass jede unabhängig voneinander betrieben werden kann, von der anderen nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="50d15-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="50d15-111">In der Vergangenheit war das Marshalling sehr ausführlich, um asynchrone Nachrichten in die Warteschlange zu stellen, zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="50d15-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="50d15-112">Mithilfe von Methoden aufrufen, die von Komponentenentwicklern leicht verständlich und verwendet werden, marshallt der com+-Dienst für Warteschlangen Komponenten automatisch Daten in Form einer Message Queuing Nachricht.</span><span class="sxs-lookup"><span data-stu-id="50d15-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="50d15-113">Und da der Dienst für in der Warteschlange befindliche Komponenten integrierte Unterstützung für Transaktionen bietet, kann ein inkonsistenter Status keine Daten beeinträchtigen, wenn ein Server Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="50d15-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="50d15-114">Die folgenden Themen in diesem Abschnitt enthalten Hintergrundinformationen zum Entwerfen und Schreiben von Komponenten in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="50d15-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="50d15-115">Thema</span><span class="sxs-lookup"><span data-stu-id="50d15-115">Topic</span></span>                                                                           | <span data-ttu-id="50d15-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50d15-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50d15-117">Vorteile der Verarbeitung in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="50d15-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="50d15-118">Beschreibt die Vorteile der Programmierung mit COM+-Komponenten in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="50d15-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="50d15-119">Architektur der Warteschlangen Komponenten</span><span class="sxs-lookup"><span data-stu-id="50d15-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="50d15-120">Beschreibt die Architektur des com+-Dienstanbieter für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="50d15-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="50d15-121">Transaktionale Message Queuing</span><span class="sxs-lookup"><span data-stu-id="50d15-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="50d15-122">Beschreibt, wie Transaktionen vom com+-Dienst in der Warteschlange verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="50d15-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="50d15-123">Sicherheit in der Warteschlange befindliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="50d15-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="50d15-124">Beschreibt die Richtlinien Optionen für die Authentifizierung von Client Nachrichten und deren Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="50d15-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="50d15-125">Entwickeln von Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="50d15-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="50d15-126">Beschreibt Überlegungen zur Programmierung beim Schreiben von Warteschlangen fähigen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="50d15-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="50d15-127">Komponenten Fehler in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="50d15-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="50d15-128">Beschreibt die häufigsten Fehlertypen, die auftreten können, wenn Sie den com+-Dienst in der Warteschlange verwenden.</span><span class="sxs-lookup"><span data-stu-id="50d15-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="50d15-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50d15-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50d15-130">Aufgaben in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="50d15-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




