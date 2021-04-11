---
description: Der wichtigste Teil beim Schreiben von Komponenten besteht im Umgang mit möglichen Fehlern.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Behandeln von Fehlern in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127793"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="f60fd-103">Behandeln von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="f60fd-103">Handling Errors in COM+</span></span>

<span data-ttu-id="f60fd-104">Der wichtigste Teil beim Schreiben von Komponenten besteht im Umgang mit möglichen Fehlern.</span><span class="sxs-lookup"><span data-stu-id="f60fd-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="f60fd-105">Der Versuch, herauszufinden, was schief gehen kann und was zu tun ist, kann unter den besten Bedingungen eine Herausforderung darstellen.</span><span class="sxs-lookup"><span data-stu-id="f60fd-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="f60fd-106">Häufige Fehler, die von der Komponente überprüft und behandelt werden können, sind fehlerhafte Netzwerkverbindungen, Sicherheitsfehler und Fehler im Zusammenhang mit nicht erreichbaren Objekten.</span><span class="sxs-lookup"><span data-stu-id="f60fd-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="f60fd-107">Darüber hinaus können Sie eigene Fehlercodes entwickeln, um Schnittstellen spezifische Fehler zu melden, z. b. Wenn eine Geschäftsregel verletzt wurde.</span><span class="sxs-lookup"><span data-stu-id="f60fd-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="f60fd-108">In Übereinstimmung mit dem COM+-Programmiermodell kann ein Objekt (und häufig) Aufrufe von Schnittstellen Methoden für andere Objekte zum Ausführen von Arbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="f60fd-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="f60fd-109">Da Programmierer Komponenten in verschiedenen Programmiersprachen schreiben können, erfordert com+, dass alle Fehler Behandlungs Mechanismen sprachneutral sind, z. b. HRESULTs-und [**errorInfo**](errorinfo.md) -Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="f60fd-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="f60fd-110">Dieser Abschnitt enthält die in der folgenden Tabelle beschriebenen Themen, in denen Techniken zur Behandlung von Fehlern in com+-Anwendungen, Features in com+, die das Fehler Verhalten beeinflussen, und Vorschläge zur Diagnose von com+-Fehlern erörtert werden.</span><span class="sxs-lookup"><span data-stu-id="f60fd-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="f60fd-111">Thema</span><span class="sxs-lookup"><span data-stu-id="f60fd-111">Topic</span></span>                                                                                           | <span data-ttu-id="f60fd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f60fd-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f60fd-113">Strategien für die Behandlung von Fehlern in com+</span><span class="sxs-lookup"><span data-stu-id="f60fd-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="f60fd-114">Listet und beschreibt die grundlegenden Richtlinien für die Behandlung von Fehlern in com+, einschließlich der Verwendung von HRESULTs-und [**errorInfo**](errorinfo.md) -Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="f60fd-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="f60fd-115">Ändern der Rückgabewerte durch com+</span><span class="sxs-lookup"><span data-stu-id="f60fd-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="f60fd-116">Identifiziert die einzige Bedingung, in der com+ ein HRESULT-Standard Objekt in einen com+-Fehlercode konvertiert, bevor es an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f60fd-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="f60fd-117">Fehler Isolation und FailFast-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f60fd-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="f60fd-118">Zeigt, wie die Fehler Isolation und die FailFast-Richtlinie das com+-Verhalten beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="f60fd-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="f60fd-119">Ermitteln der Fehlerquelle</span><span class="sxs-lookup"><span data-stu-id="f60fd-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="f60fd-120">Beschreibt, wie Sie die Quelle diagnostizieren und eine Beschreibung von Anwendungsfehlern abrufen können.</span><span class="sxs-lookup"><span data-stu-id="f60fd-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="f60fd-121">Interpretieren von Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="f60fd-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="f60fd-122">Identifiziert den vorherrschenden Fehler Behandlungs Mechanismus für Microsoft Visual C++, die Java-Sprache und Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f60fd-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="f60fd-123">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="f60fd-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="f60fd-124">Bietet zusätzliche Unterstützung bei der Diagnose von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="f60fd-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f60fd-125">Kontaktieren des Supports</span><span class="sxs-lookup"><span data-stu-id="f60fd-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="f60fd-126">Identifiziert wichtige Informationen zur Problembehebung, die Sie beim Kontaktieren des Supports bereitstellen sollten.</span><span class="sxs-lookup"><span data-stu-id="f60fd-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="f60fd-127">Ausführliche Informationen zur Behandlung von Fehlern, die mit verschiedenen COM+-Diensten verbunden sind, finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="f60fd-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="f60fd-128">Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts</span><span class="sxs-lookup"><span data-stu-id="f60fd-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="f60fd-129">[Behandeln von Fehlern](handling-errors-in-queued-components.md) (für in der Warteschlange befindliche Komponenten)</span><span class="sxs-lookup"><span data-stu-id="f60fd-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f60fd-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f60fd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f60fd-131">Com+-Anwendungen debuggen</span><span class="sxs-lookup"><span data-stu-id="f60fd-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




