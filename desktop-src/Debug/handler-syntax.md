---
description: In diesem Abschnitt werden die Syntax und die Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungs Compiler implementiert ist. Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Mechanismus zur Ausnahmebehandlung interpretiert.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: HandlerSyntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860680"
---
# <a name="handler-syntax"></a><span data-ttu-id="c3f05-104">HandlerSyntax</span><span class="sxs-lookup"><span data-stu-id="c3f05-104">Handler Syntax</span></span>

<span data-ttu-id="c3f05-105">In diesem Abschnitt werden die Syntax und die Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungs Compiler implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c3f05-105">This section describes the syntax and usage of structured exception handling as implemented in the Microsoft C/C++ Optimizing Compiler.</span></span> <span data-ttu-id="c3f05-106">Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Mechanismus zur Ausnahmebehandlung interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c3f05-106">The following keywords are interpreted by the compiler as part of the structured exception-handling mechanism.</span></span>



| <span data-ttu-id="c3f05-107">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="c3f05-107">Keyword</span></span>         | <span data-ttu-id="c3f05-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3f05-108">Description</span></span>                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f05-109">**\_\_versu**</span><span class="sxs-lookup"><span data-stu-id="c3f05-109">**\_\_try**</span></span>     | <span data-ttu-id="c3f05-110">Beginnt einen überwachten Code Körper.</span><span class="sxs-lookup"><span data-stu-id="c3f05-110">Begins a guarded body of code.</span></span> <span data-ttu-id="c3f05-111">Wird mit dem Schlüsselwort **\_ \_ außer** verwendet, um einen [Ausnahmehandler](exception-handler-syntax.md)zu erstellen, oder mit dem Schlüsselwort " **\_ \_ endgültig** " zum Erstellen eines Beendigungs [Handlers](termination-handler-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="c3f05-111">Used with the **\_\_except** keyword to construct an [exception handler](exception-handler-syntax.md), or with the **\_\_finally** keyword to construct a [termination handler](termination-handler-syntax.md).</span></span> |
| <span data-ttu-id="c3f05-112">**\_\_davon**</span><span class="sxs-lookup"><span data-stu-id="c3f05-112">**\_\_except**</span></span>  | <span data-ttu-id="c3f05-113">Startet einen Codeblock, der nur ausgeführt wird, wenn eine Ausnahme innerhalb des zugeordneten **\_ \_ try** -Blocks auftritt.</span><span class="sxs-lookup"><span data-stu-id="c3f05-113">Begins a block of code that is executed only when an exception occurs within its associated **\_\_try** block.</span></span>                                                                                                                                   |
| <span data-ttu-id="c3f05-114">**\_\_finally**</span><span class="sxs-lookup"><span data-stu-id="c3f05-114">**\_\_finally**</span></span> | <span data-ttu-id="c3f05-115">Startet einen Codeblock, der ausgeführt wird, wenn die Ablauf Steuerung den zugeordneten **\_ \_ try** -Block verlässt.</span><span class="sxs-lookup"><span data-stu-id="c3f05-115">Begins a block of code that is executed whenever the flow of control leaves its associated **\_\_try** block.</span></span>                                                                                                                                    |
| <span data-ttu-id="c3f05-116">**\_\_lassen Sie**</span><span class="sxs-lookup"><span data-stu-id="c3f05-116">**\_\_leave**</span></span>   | <span data-ttu-id="c3f05-117">Ermöglicht das sofortige Beenden des **\_ \_ try** -Blocks, ohne dass eine nicht ordnungsgemäße Beendigung und die Leistungseinbußen verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="c3f05-117">Allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span>                                                                                                                      |



 

<span data-ttu-id="c3f05-118">Der Compiler interpretiert außerdem die Funktionen [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)und [**abnormalabbruch**](abnormaltermination.md) als Schlüsselwörter, und ihre Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.</span><span class="sxs-lookup"><span data-stu-id="c3f05-118">The compiler also interprets the [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md), and [**AbnormalTermination**](abnormaltermination.md) functions as keywords, and their use outside the appropriate exception-handling syntax generates a compiler error.</span></span> <span data-ttu-id="c3f05-119">Im folgenden finden Sie eine kurze Beschreibung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c3f05-119">The following are brief descriptions of these functions.</span></span>



| <span data-ttu-id="c3f05-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="c3f05-120">Function</span></span>                                                   | <span data-ttu-id="c3f05-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3f05-121">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3f05-122">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="c3f05-122">**GetExceptionCode**</span></span>](getexceptioncode.md)               | <span data-ttu-id="c3f05-123">Gibt einen Code zurück, der den Typ der Ausnahme identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c3f05-123">Returns a code that identifies the type of exception.</span></span> <span data-ttu-id="c3f05-124">Diese Funktion kann nur innerhalb des Filter Ausdrucks oder des ausnahmehandlerblocks aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3f05-124">This function can be called only from within the filter expression or the exception-handler block.</span></span>                                                                                                |
| [<span data-ttu-id="c3f05-125">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="c3f05-125">**GetExceptionInformation**</span></span>](getexceptioninformation.md) | <span data-ttu-id="c3f05-126">Gibt einen Zeiger auf eine [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Struktur zurück, die Zeiger auf den Kontext Daten Satz und den Ausnahme Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="c3f05-126">Returns a pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure containing pointers to the context record and the exception record.</span></span> <span data-ttu-id="c3f05-127">Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3f05-127">This function can be called only from within the filter expression of an exception handler.</span></span> |
| [<span data-ttu-id="c3f05-128">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="c3f05-128">**AbnormalTermination**</span></span>](abnormaltermination.md)         | <span data-ttu-id="c3f05-129">Gibt an, ob die Ablauf Steuerung den zugeordneten **\_ \_ try** -Block nacheinander nach dem Ausführen der letzten Anweisung im-Block verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="c3f05-129">Indicates whether the flow of control left the associated **\_\_try** block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="c3f05-130">Diese Funktion kann nur innerhalb des **\_ \_ letzten Blocks eines** Beendigungs Handlers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3f05-130">This function can be called only from within the **\_\_finally** block of a termination handler.</span></span>              |



 

 

 



