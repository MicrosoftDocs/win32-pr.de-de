---
title: Informationen zu wer
description: Windows-Fehlerberichterstattung (wer) ist eine flexible ereignisbasierte Feedback Infrastruktur, die für die Erfassung von Informationen zu den Hardware-und Softwareproblemen konzipiert ist, die von Windows erkannt werden können, die Informationen an Microsoft zu melden und Benutzern alle verfügbaren Lösungen bereitzustellen. Informationen zu den Verbesserungen an wer finden Sie unter What es New in Wer.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Windows-Fehlerberichterstattung für die Windows-Fehlerberichterstattung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310492"
---
# <a name="about-wer"></a><span data-ttu-id="46a0f-105">Informationen zu wer</span><span class="sxs-lookup"><span data-stu-id="46a0f-105">About WER</span></span>

<span data-ttu-id="46a0f-106">Windows-Fehlerberichterstattung (wer) ist eine flexible ereignisbasierte Feedback Infrastruktur, die für die Erfassung von Informationen zu den Hardware-und Softwareproblemen konzipiert ist, die von Windows erkannt werden können, die Informationen an Microsoft zu melden und Benutzern alle verfügbaren Lösungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="46a0f-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="46a0f-107">Informationen zu den Verbesserungen an wer finden Sie unter [What es New in Wer](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="46a0f-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="46a0f-108">Ab Windows Vista stellt Windows Absturz-, nicht-Antwort-und Kernel Fehler-Fehlerberichterstattung standardmäßig bereit, ohne dass Änderungen an der Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="46a0f-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="46a0f-109">Anwendungen verwenden stattdessen die wer-API, um Fehlerberichte für anwendungsspezifische Probleme zu generieren, die nicht mit Abstürzen, nicht-Antworten oder Kernel Fehlern zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="46a0f-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="46a0f-110">Um Fehlerberichte für anwendungsspezifische Probleme zu generieren, muss die Anwendung eine kurze Beschreibung des Problems mithilfe einiger grundlegender Informationen erstellen, die als *Berichts Parameter* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="46a0f-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="46a0f-111">Berichts Parameter enthalten Informationen wie den Anwendungsnamen, die Anwendungs Version, den Modulnamen, die Modulversion und den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="46a0f-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="46a0f-112">Durch die Kombination dieser Berichts Parameter wird ein eindeutiges Problem beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46a0f-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="46a0f-113">Wenn wer auf eine Lösung prüft, kommuniziert er mit dem wer-Server bei Microsoft, indem er zunächst fragt, ob das Problem bereits bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="46a0f-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="46a0f-114">Der Server antwortet auf eine der folgenden Arten:</span><span class="sxs-lookup"><span data-stu-id="46a0f-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="46a0f-115">Wenn das Problem bekannt ist und eine Lösung vorhanden ist, sendet der Server die Lösung an den Client Computer, und wer zeigt diese Informationen dem Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="46a0f-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="46a0f-116">Wenn das Problem untersucht wird, sendet der Server möglicherweise eine Antwort, die den Status angibt.</span><span class="sxs-lookup"><span data-stu-id="46a0f-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="46a0f-117">Wenn der Entwickler Weitere Informationen benötigt, um das Problem zu beheben, fordert der Server zusätzliche Informationen von wer an und fordert den Benutzer auf, die Berechtigung zum Senden dieser Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46a0f-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="46a0f-118">Wenn das Problem nicht bekannt ist, erstellt der Server ein Problem, das ein Entwickler untersuchen und eine Antwort sendet, die den Status angibt.</span><span class="sxs-lookup"><span data-stu-id="46a0f-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="46a0f-119">Wenn Sie diesen Prozess verwenden, sammelt er bei Bedarf weitere Informationen oder sendet eine Lösung an den Benutzer, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46a0f-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="46a0f-120">Unter Windows Vista kann der Benutzer jederzeit zu **Problem berichten und-Lösungen** wechseln, um verfügbare Lösungen anzuzeigen, zu überprüfen, ob neue Lösungen verfügbar sind, oder andere wer-Berichte und-Einstellungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="46a0f-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="46a0f-121">Unter Windows 7 werden die **Problem Berichte und-Lösungen** jetzt als " **Aktions Center**" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="46a0f-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="46a0f-122">Klicken Sie auf **Start** , und geben Sie "View" in **Programme/Dateien durchsuchen** ein, und wählen Sie dann **Alle Problemberichte anzeigen**, **Zuverlässigkeits Verlauf anzeigen** oder **Lösungen für Probleme anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="46a0f-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a0f-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46a0f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a0f-124">Windows-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="46a0f-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




