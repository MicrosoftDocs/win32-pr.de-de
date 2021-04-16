---
title: Testen mit accchecker
description: Beschreibt den typischen Test Workflow, der accchecker integriert.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- Testen mit accchecker
- Accchecker, Testen des Workflows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515524"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="1a9da-105">Testen mit accchecker</span><span class="sxs-lookup"><span data-stu-id="1a9da-105">Testing with AccChecker</span></span>

<span data-ttu-id="1a9da-106">Im folgenden Szenario werden die Schritte beschrieben, die Sie normalerweise beim Testen mit der-Zugriffsmethode ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a9da-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="1a9da-107">Wenn accchecker-Überprüfungs Routinen ausgeführt werden, kann die Benutzerinteraktion mit dem Host Computer einige Routinen stören.</span><span class="sxs-lookup"><span data-stu-id="1a9da-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="1a9da-108">Es wird empfohlen, keine weitere Benutzerinteraktion auszuführen, bis die Zugriffs Überprüfung den Benutzer darüber benachrichtigt, dass alle Aufgaben vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="1a9da-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="1a9da-109">Ausführen von accchecker-Verifizierungen für eine bestimmte Zielanwendung oder ein bestimmtes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1a9da-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="1a9da-110">Weitere Informationen finden Sie auf der [Registerkarte Überprüfungen](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1a9da-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="1a9da-111">Die Zugriffs Prüfung untersucht nicht alle UI-Permutationen in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1a9da-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="1a9da-112">Elemente, die in Steuerelementen wie Fenstern, Bereichen, Registerkarten und Menüs ausgeblendet sind, müssen manuell verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="1a9da-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="1a9da-113">Überprüfen Sie das Fehlerprotokoll der Zugriffs Überprüfung, und bewerten oder selelieren Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="1a9da-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="1a9da-114">Beheben Sie triviale Probleme, und protokollieren Sie gegebenenfalls schwerwiegende Fehler.</span><span class="sxs-lookup"><span data-stu-id="1a9da-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="1a9da-115">Generieren Sie eine Unterdrückungs Datei für Fehler und Fehler, die bis zum Testen der Regression ignoriert werden können.</span><span class="sxs-lookup"><span data-stu-id="1a9da-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="1a9da-116">Führen Sie accchecker-Überprüfungen mit der Unterdrückungs Datei und den anfänglichen Fehlerbehebungen erneut aus.</span><span class="sxs-lookup"><span data-stu-id="1a9da-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="1a9da-117">Dies bietet eine Momentaufnahme der Probleme in der aktuellen Implementierung von Microsoft Active Accessibility und legt eine Baseline für Regressionstests fest.</span><span class="sxs-lookup"><span data-stu-id="1a9da-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="1a9da-118">Integrieren Sie die accchecker-APIs und die Unterdrückungs Datei in ein automatisiertes Test Framework, um Regressionstests für Fehler zu überprüfen, die bei der anfänglichen Zugriffs Überprüfung protokolliert wurden</span><span class="sxs-lookup"><span data-stu-id="1a9da-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="1a9da-119">Da Fehler behoben werden, sollte die Unterdrückungs Datei bei Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1a9da-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="1a9da-120">Vergewissern Sie sich, dass in der Anwendung oder im Steuerelement keine Regressionen oder neuen Barrierefreiheits Fehler eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="1a9da-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a9da-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a9da-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a9da-122">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="1a9da-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




