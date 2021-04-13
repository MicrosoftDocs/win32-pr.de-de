---
title: Neues in Wer
description: Auf dieser Seite werden die neuen Features von Windows-Fehlerberichterstattung (wer) für die einzelnen Releases zusammengefasst.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Windows-Fehlerberichterstattung Windows-Fehlerberichterstattung, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314648"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="715a8-104">Neues in Wer</span><span class="sxs-lookup"><span data-stu-id="715a8-104">What's New in WER</span></span>

<span data-ttu-id="715a8-105">Auf dieser Seite werden die neuen Features von Windows-Fehlerberichterstattung (wer) für die einzelnen Releases zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="715a8-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="715a8-106">Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="715a8-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="715a8-107">In der folgenden Liste werden die neuen wer-Features für Windows 7 und Windows Server 2008 R2 zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="715a8-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="715a8-108">Fügt die Möglichkeit hinzu, eine Ausnahme zu auslösen, die alle Ausnahmehandler umgeht, wodurch die Anwendung sofort beendet und Windows-Fehlerberichterstattung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="715a8-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="715a8-109">Weitere Informationen finden Sie unter der [**raisegfailfastexception**](/previous-versions/dd408166(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="715a8-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="715a8-110">Fügt die Möglichkeit hinzu, einen Out-of-Process-Ausnahmehandler zu registrieren, den wer beim Auftreten eines Absturzes aufruft, um den Ereignis Namen, die Berichts Parameter und die Optionen zum Debuggen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="715a8-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="715a8-111">Weitere Informationen finden Sie unter der Funktion " [**werregisterruntimeexceptionmodule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) ".</span><span class="sxs-lookup"><span data-stu-id="715a8-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="715a8-112">Hinzugefügte Funktionen:</span><span class="sxs-lookup"><span data-stu-id="715a8-112">Functions that were added:</span></span>

-   [<span data-ttu-id="715a8-113">**Outo-processexceptioneventcallback**</span><span class="sxs-lookup"><span data-stu-id="715a8-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="715a8-114">**Outo-processexceptioneventsignaturecallback**</span><span class="sxs-lookup"><span data-stu-id="715a8-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="715a8-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="715a8-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="715a8-116">[**Raian failfastexception**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="715a8-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="715a8-117">**Werregisterruntimeexceptionmodule**</span><span class="sxs-lookup"><span data-stu-id="715a8-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="715a8-118">**Werunregisterruntimeexceptionmodule**</span><span class="sxs-lookup"><span data-stu-id="715a8-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="715a8-119">Hinzugefügte Strukturen:</span><span class="sxs-lookup"><span data-stu-id="715a8-119">Structures that were added:</span></span>

-   [<span data-ttu-id="715a8-120">**\_Informationen zur Lauf Zeit \_ Ausnahme \_**</span><span class="sxs-lookup"><span data-stu-id="715a8-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="715a8-121">Windows Server 2008 und Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="715a8-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="715a8-122">In der folgenden Liste sind die neuen Features von wer für Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="715a8-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="715a8-123">Wer kann so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt (Anwendungen, die eigene benutzerdefinierte Absturzberichte ausführen, einschließlich .NET-Anwendungen, werden nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="715a8-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="715a8-124">Weitere Informationen finden Sie unter [Sammeln von User-Mode Dumps](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="715a8-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="715a8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="715a8-125">Windows Vista</span></span>

<span data-ttu-id="715a8-126">In der folgenden Liste werden die neuen Features von Windows-Fehlerberichterstattung (wer) für Windows Vista zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="715a8-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="715a8-127">Wer wurde über das Überwachen von Abstürzen und nicht reagierenden Prozessen hinaus erweitert.</span><span class="sxs-lookup"><span data-stu-id="715a8-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="715a8-128">Wer bietet Unterstützung für viele neue Typen nicht kritischer Ereignisse, z. b. Leistungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="715a8-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="715a8-129">Dies ermöglicht es Entwicklern, mehr über die Erfahrungen zu erfahren, die Ihre Kunden mit den Anwendungen haben, die Sie entwickelt haben.</span><span class="sxs-lookup"><span data-stu-id="715a8-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="715a8-130">Neue Funktionen bieten Entwicklern die Flexibilität, Problemberichte zu erstellen, anzupassen und zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="715a8-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="715a8-131">Weitere Informationen finden Sie unter [wer Functions](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="715a8-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="715a8-132">Die verbesserten [Online Dienste für Windows-Qualität](https://www.microsoft.com/?ref=go) bieten Entwicklern Zugang zu den Problem Informationen, die Kunden für Ihre Anwendungen einreichen, sowie einen Mechanismus zum Bereitstellen von Lösungen für diese Kunden.</span><span class="sxs-lookup"><span data-stu-id="715a8-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="715a8-133">Mit den Funktionen, die von [Anwendungs Wiederherstellung und Neustart](/windows/desktop/Recovery/application-recovery-and-restart-portal) und [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) eingeführt werden, können Anwendungen automatisch Informationen wiederherstellen und im Falle eines schwerwiegenden Fehlers neu starten.</span><span class="sxs-lookup"><span data-stu-id="715a8-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="715a8-134">Entwickler können diese Features in Ihren Anwendungen verwenden, um die Benutzer Leistung erheblich zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="715a8-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="715a8-135">**Problem Berichte und-Lösungen unter Windows Vista oder das Aktions Center auf Windows 7** sind der zentrale Ort, an dem Benutzer mit wer interagieren können.</span><span class="sxs-lookup"><span data-stu-id="715a8-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="715a8-136">Benutzer können nach neuen Lösungen suchen, ihren Berichts Verlauf verwalten, die Details eines Problem Berichts anzeigen und die Bericht Erstellungs Einstellungen verwalten. Dies schließt auch das Aktivieren von Wer ein, um automatisch nach Lösungen zu suchen, ohne den Benutzer zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="715a8-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="715a8-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="715a8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="715a8-138">Windows-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="715a8-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 