---
description: Die Mechanismen für die strukturierte Ausnahmebehandlung und die Beendigung der Beendigung sind integrale Bestandteile des Systems. Dadurch kann das System robust sein. Mit diesen Mechanismen können Sie konsistent stabile und zuverlässige Anwendungen erstellen.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: Informationen über die strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214073"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="c1550-104">Informationen über die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="c1550-104">About Structured Exception Handling</span></span>

<span data-ttu-id="c1550-105">Die Mechanismen für die strukturierte Ausnahmebehandlung und die Beendigung der Beendigung sind integrale Bestandteile des Systems. Dadurch kann das System robust sein.</span><span class="sxs-lookup"><span data-stu-id="c1550-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="c1550-106">Mit diesen Mechanismen können Sie konsistent stabile und zuverlässige Anwendungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1550-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="c1550-107">Die strukturierte Ausnahmebehandlung wird primär durch Compiler-Unterstützung zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="c1550-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="c1550-108">Beispielsweise unterstützt der Microsoft C/C++-Optimierungs Compiler das **\_ \_ try** -Schlüsselwort, das einen geschützten Codetext identifiziert, das **\_ \_ außer** -Schlüsselwort, das einen Ausnahmehandler identifiziert, und das Schlüsselwort " **\_ \_ endgültig** ", das einen Beendigungs Handler identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c1550-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="c1550-109">Obwohl in dieser Übersicht spezifische Beispiele für den Microsoft C/C++-Compiler verwendet werden, bieten auch andere Compiler diese Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="c1550-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="c1550-110">Behandlung von Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c1550-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="c1550-111">Frame basierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="c1550-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="c1550-112">Behandlung von Vektoren Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="c1550-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="c1550-113">Abbruch Behandlung</span><span class="sxs-lookup"><span data-stu-id="c1550-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="c1550-114">HandlerSyntax</span><span class="sxs-lookup"><span data-stu-id="c1550-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



