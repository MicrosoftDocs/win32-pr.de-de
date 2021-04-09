---
description: Eine Ausnahme ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablauf Steuerungs Codes erfordert.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860675"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="10ff3-103">Strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="10ff3-103">Structured Exception Handling</span></span>

<span data-ttu-id="10ff3-104">Eine *Ausnahme* ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablauf Steuerungs Codes erfordert.</span><span class="sxs-lookup"><span data-stu-id="10ff3-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="10ff3-105">Es gibt zwei Arten von Ausnahmen: Hardware Ausnahmen und Software Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="10ff3-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="10ff3-106">*Hardware Ausnahmen* werden von der CPU initiiert.</span><span class="sxs-lookup"><span data-stu-id="10ff3-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="10ff3-107">Sie können sich aus der Ausführung bestimmter Anweisungs Sequenzen ergeben, z. b. der Division durch 0 (null) oder einem Versuch, auf eine ungültige Speicheradresse zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="10ff3-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="10ff3-108">*Software Ausnahmen* werden explizit von Anwendungen oder dem Betriebssystem initiiert.</span><span class="sxs-lookup"><span data-stu-id="10ff3-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="10ff3-109">Beispielsweise kann das System erkennen, wenn ein Ungültiger Parameterwert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10ff3-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="10ff3-110">Die *strukturierte Ausnahmebehandlung* ist ein Mechanismus für die Behandlung von Hardware-und Software Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="10ff3-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="10ff3-111">Daher verarbeitet der Code Hardware-und Software Ausnahmen identisch.</span><span class="sxs-lookup"><span data-stu-id="10ff3-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="10ff3-112">Die strukturierte Ausnahmebehandlung ermöglicht Ihnen die vollständige Kontrolle über die Behandlung von Ausnahmen, bietet Unterstützung für debuggerund kann für alle Programmiersprachen und Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10ff3-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="10ff3-113">Die *Behandlung von Vektoren Ausnahmen* ist eine Erweiterung der strukturierten Ausnahmebehandlung.</span><span class="sxs-lookup"><span data-stu-id="10ff3-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="10ff3-114">Das System unterstützt auch die *Beendigung der Beendigung*, sodass Sie sicherstellen können, dass bei jeder Ausführung eines geschützten Code Texts auch ein angegebener Block von Beendigungs Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10ff3-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="10ff3-115">Der Beendigungs Code wird ausgeführt, unabhängig davon, wie die Ablauf Steuerung den überwachten Text verlässt.</span><span class="sxs-lookup"><span data-stu-id="10ff3-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="10ff3-116">Ein Beendigungs Handler kann z. b. sicherstellen, dass Bereinigungs Tasks ausgeführt werden, auch wenn eine Ausnahme oder ein anderer Fehler auftritt, während der überwachte Code Körper ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10ff3-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="10ff3-117">Informationen über die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="10ff3-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="10ff3-118">Verwenden der strukturierten Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="10ff3-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="10ff3-119">Referenz für die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="10ff3-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



