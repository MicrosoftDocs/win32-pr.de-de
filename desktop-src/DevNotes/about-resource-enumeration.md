---
description: Die ressourcenenumeration bietet eine genaue Ansicht der Instrumentations Aktivität, die stattfindet, wenn eine Anwendung ausgeführt wird.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: Informationen zur ressourcenenumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344340"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="57041-103">Informationen zur ressourcenenumeration</span><span class="sxs-lookup"><span data-stu-id="57041-103">About Resource Enumeration</span></span>

<span data-ttu-id="57041-104">Die ressourcenenumeration bietet eine genaue Ansicht der Instrumentations Aktivität, die stattfindet, wenn eine Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57041-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="57041-105">Die Instrumentierungs Informationen können als Teil des Debugprozesses als Satz Prozess spezifischer Elemente abstrahiert und kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="57041-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="57041-106">Tools, wie z. b. Debugger, benötigen häufig Zugriff auf Instrumentations Informationen, sind aber möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57041-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="57041-107">Um dieses Problem zu beheben, extrahiert die [**verifierenumerateresource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) -Funktion diese Art von Informationen aus Anwendungen, um bessere Kontextinformationen für das Problem bereitzustellen, das gedebuggt wird.</span><span class="sxs-lookup"><span data-stu-id="57041-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



