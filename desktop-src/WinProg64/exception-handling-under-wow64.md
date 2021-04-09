---
title: Ausnahmebehandlung unter WOW64
description: WOW64 verwendet Native x64-, ia64-oder ARM64-Ausnahmen als Transport für x86-Ausnahmen. Daher verhalten sich nicht abgefangene Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039470"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="48006-104">Ausnahmebehandlung unter WOW64</span><span class="sxs-lookup"><span data-stu-id="48006-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="48006-105">WOW64 verwendet Native x64-, ia64-oder ARM64-Ausnahmen als Transport für x86-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="48006-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="48006-106">Daher verhalten sich nicht abgefangene Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="48006-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="48006-107">In einer Anwendung, die auf einer 32-Bit-Version von Windows ausgeführt wird, werden nicht abgefangene Ausnahmen an die übergeordneten Ausnahmehandler der Anwendung weitergegeben, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="48006-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="48006-108">In derselben 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, unterdrückt das System möglicherweise nicht abgefangene Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="48006-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="48006-109">**Windows Vista, Windows Server 2003 und Windows XP:** In derselben 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, ruft das System die Ausnahme Filter auf, unterdrückt jedoch möglicherweise nicht abgefangene Ausnahmen, ohne die zugehörigen Handler aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="48006-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="48006-110">Dieses Verhalten hat sich seit Windows Vista mit Service Pack 1 (SP1) geändert.</span><span class="sxs-lookup"><span data-stu-id="48006-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="48006-111">Weitere Informationen zu nicht abgefangenen Ausnahmen in Windows-Prozeduren finden Sie unter der [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="48006-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 