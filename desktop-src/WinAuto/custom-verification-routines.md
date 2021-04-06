---
title: Benutzerdefinierte Überprüfungs Routinen
description: In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Überprüfungs Routine für das Tool für die Benutzeroberflächen Zugriffs Prüfung (accchecker) erstellt wird.
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947498"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="b6de5-103">Benutzerdefinierte Überprüfungs Routinen</span><span class="sxs-lookup"><span data-stu-id="b6de5-103">Custom Verification Routines</span></span>

<span data-ttu-id="b6de5-104">In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Überprüfungs Routine für das Tool für die Benutzeroberflächen Zugriffs Prüfung (accchecker) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b6de5-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="b6de5-105">Erstellen einer benutzerdefinierten Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="b6de5-106">Benutzerdefinierte Beispiel Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="b6de5-107">Verwenden einer benutzerdefinierten Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="b6de5-108">Die grafische Benutzeroberfläche der Zugriffs Prüfung (GUI)</span><span class="sxs-lookup"><span data-stu-id="b6de5-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="b6de5-109">Accchecker-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="b6de5-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="b6de5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6de5-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="b6de5-111">Die UI-Barrierefreiheits Prüfung (accchecker) ist ein Tool zur Barrierefreiheit, mit dem die Implementierung von Microsoft Active Accessibility (MSAA) in einer Steuerelement-oder Anwendungs Benutzeroberfläche überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6de5-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="b6de5-112">Die Auswirkungen auf Barrierefreiheits Probleme, die möglicherweise durch die MSAA-Implementierung verfügbar gemacht werden, werden mit einer Reihe integrierter automatisierter Überprüfungs Routinen getestet.</span><span class="sxs-lookup"><span data-stu-id="b6de5-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="b6de5-113">Diese nativen Überprüfungs Routinen können mithilfe der Extensible accchecker-Plattform durch angepasste Routinen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="b6de5-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="b6de5-114">Erstellen einer benutzerdefinierten Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-114">Creating a Custom Verification</span></span>

<span data-ttu-id="b6de5-115">Eine benutzerdefinierte Überprüfung wird als Klassenbibliothek (dll) erstellt, die eine einzelne Schnittstelle ( `IVerificationRoutine` ) mit einem Member ( `Execute` ) implementiert:</span><span class="sxs-lookup"><span data-stu-id="b6de5-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="b6de5-116">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="b6de5-116">**Parameters**</span></span>

<span data-ttu-id="b6de5-117">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b6de5-117">*hwnd*</span></span>

<span data-ttu-id="b6de5-118">Typ: **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="b6de5-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="b6de5-119">Das HWND des Elements, das überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="b6de5-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="b6de5-120">*Protokollierung*</span><span class="sxs-lookup"><span data-stu-id="b6de5-120">*logger*</span></span>

<span data-ttu-id="b6de5-121">Typ: **acccheck. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="b6de5-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="b6de5-122">Die ausgewählte Protokollierungs Methode.</span><span class="sxs-lookup"><span data-stu-id="b6de5-122">The selected logging method.</span></span> <span data-ttu-id="b6de5-123">Mögliche Typen sind **akkumulatinglogger** (von der Zugriffs Prüfung verwendet, um alle Protokolleinträge zwischenzuspeichern, bis die Überprüfungen vollständig sind), **ConsoleLogger**, **textfilelogger** und **xmlserializinglogger**.</span><span class="sxs-lookup"><span data-stu-id="b6de5-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="b6de5-124">*Zuordnung*</span><span class="sxs-lookup"><span data-stu-id="b6de5-124">*AllowUI*</span></span>

<span data-ttu-id="b6de5-125">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="b6de5-125">Type: **bool**</span></span>

<span data-ttu-id="b6de5-126">Gibt an, ob die Überprüfungs Routine die zu testenden Benutzeroberfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b6de5-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="b6de5-127">In automatisierten Testszenarien wird in der Regel auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b6de5-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="b6de5-128">*Grafik*</span><span class="sxs-lookup"><span data-stu-id="b6de5-128">*graphics*</span></span>

<span data-ttu-id="b6de5-129">Typ: **acccheck. graphicshelper**</span><span class="sxs-lookup"><span data-stu-id="b6de5-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="b6de5-130">Wird für Screenshots und andere Visualisierungen innerhalb der accchecker verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6de5-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="b6de5-131">Benutzerdefinierte Beispiel Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-131">Sample Custom Verification</span></span>

<span data-ttu-id="b6de5-132">Das folgende Beispiel ist eine benutzerdefinierte c#-Überprüfung, die eine einfache Elementstruktur-tiefen Prüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="b6de5-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="b6de5-133">Ein Fehler wird protokolliert, wenn die Elementstruktur größer als 50 Ebenen tief ist. eine Warnung wird protokolliert, wenn die Elementstruktur 20 bis 50 Ebenen tief ist, und andernfalls eine Informations Meldung protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="b6de5-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="b6de5-134">In der Hilfe Dokumentation finden Sie eine Microsoft Visual Studio Lösung mit Überprüfungs Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="b6de5-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="b6de5-135">Die Dateien befinden sich im accchecker-Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="b6de5-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="b6de5-136">Verwenden einer benutzerdefinierten Überprüfung</span><span class="sxs-lookup"><span data-stu-id="b6de5-136">Using a Custom Verification</span></span>

<span data-ttu-id="b6de5-137">In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Überprüfung in accchecker-Testszenarien integrieren.</span><span class="sxs-lookup"><span data-stu-id="b6de5-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="b6de5-138">Die grafische Benutzeroberfläche der Zugriffs Prüfung (GUI)</span><span class="sxs-lookup"><span data-stu-id="b6de5-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="b6de5-139">Wenn Sie eine benutzerdefinierte Überprüfungs Routine in die accchecker-Anwendung einschließen möchten, klicken Sie einfach im Menü Datei auf dll öffnen, und suchen Sie die DLL für die Routine.</span><span class="sxs-lookup"><span data-stu-id="b6de5-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="b6de5-140">Die benutzerdefinierte Routine wird am Ende der Liste der Überprüfungen im Bereich Überprüfungs Routinen auswählen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b6de5-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="b6de5-141">Der folgende Screenshot zeigt die benutzerdefinierte Überprüfung der Überprüfung der Struktur Tiefe, die der Zugriffs Prüfung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b6de5-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![Beispiel für Überprüfung der benutzerdefinierten Überprüfungs Routine für die Benutzeroberfläche der accchecker-Benutzeroberfläche](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="b6de5-143">Wenn die Überprüfungs Attributwerte nicht in der benutzerdefinierten Überprüfungs Routine angegeben werden, wird die Überprüfung weiterhin in die Zugriffs Prüfung geladen, auch wenn Sie nicht in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b6de5-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="b6de5-144">Da es nicht in der Benutzeroberfläche angezeigt wird, kann es nicht deaktiviert und von nachfolgenden Überprüfungs Läufen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b6de5-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="b6de5-145">Accchecker-Automatisierung</span><span class="sxs-lookup"><span data-stu-id="b6de5-145">AccChecker Automation</span></span>

<span data-ttu-id="b6de5-146">Das Integrieren einer benutzerdefinierten Überprüfungs Routine in ein automatisiertes accchecker-Framework ist so einfach wie das Hinzufügen der Überprüfungs-dll und das Aktivieren der gewünschten Überprüfungs Routinen.</span><span class="sxs-lookup"><span data-stu-id="b6de5-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="b6de5-147">Der folgende Code Ausschnitt veranschaulicht, wie die accesschecker-API verwendet wird, um die Tabstopps-Funktionalität in der System Steuerungsanwendung der Windows-Firewall zu testen.</span><span class="sxs-lookup"><span data-stu-id="b6de5-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> In der Hilfe Dokumentation finden Sie eine Microsoft Visual Studio 2008-Lösung mit Überprüfungs Beispielcode. <span data-ttu-id="b6de5-149">Die Dateien befinden sich im accchecker-Installationspfad.</span><span class="sxs-lookup"><span data-stu-id="b6de5-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b6de5-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6de5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6de5-151">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="b6de5-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




