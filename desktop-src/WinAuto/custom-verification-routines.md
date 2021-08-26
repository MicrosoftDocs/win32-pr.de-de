---
title: Benutzerdefinierte Überprüfungsroutinen
description: In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Überprüfungsroutine für das AccChecker-Tool (UI Accessibility Checker) erstellen.
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245865a0ab4aa6848d4a4361a30febbb341742208586ebf4ec5b35c34fa30534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030884"
---
# <a name="custom-verification-routines"></a>Benutzerdefinierte Überprüfungsroutinen

In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Überprüfungsroutine für das AccChecker-Tool (UI Accessibility Checker) erstellen.

-   [Erstellen einer benutzerdefinierten Überprüfung](#creating-a-custom-verification)
    -   [Beispiel für benutzerdefinierte Überprüfung](#sample-custom-verification)
-   [Verwenden einer benutzerdefinierten Überprüfung](#using-a-custom-verification)
    -   [Die grafische AccChecker-Benutzeroberfläche (GUI)](#the-accchecker-graphical-user-interface-gui)
    -   [AccChecker Automation](#accchecker-automation)
-   [Zugehörige Themen](#related-topics)

Ui Accessibility Checker (AccChecker) ist ein Tool zum Testen der Barrierefreiheit, mit dem die Implementierung von Microsoft Active Accessibility (MSAA) in einer Steuerelement- oder Anwendungsbenutzeroberfläche überprüft werden kann. Probleme mit hoher Barrierefreiheit, die möglicherweise von der MSAA-Implementierung verfügbar gemacht werden, werden mit einer Reihe integrierter automatisierter Überprüfungsroutinen getestet. Diese nativen Überprüfungsroutinen können mithilfe der erweiterbaren AccChecker-Plattform um benutzerdefinierte Routinen erweitert werden.

## <a name="creating-a-custom-verification"></a>Erstellen einer benutzerdefinierten Überprüfung

Eine benutzerdefinierte Überprüfung wird als Klassenbibliothek (DLL) erstellt, die eine einzelne Schnittstelle ( ) implementiert, `IVerificationRoutine` die einen Member ( ) `Execute` enthält:


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parameter**

*Hwnd*

Typ: **System.IntPtr**

Der HWND des elements, das überprüft wird.

*Logger*

Typ: **AccCheck.Logging.ILogger**

Die ausgewählte Protokollierungsmethode. Mögliche Typen sind **AccumulatingLogger** (wird von AccChecker verwendet, um alle Protokolleinträge zwischenzuspeichern, bis die Überprüfungen abgeschlossen sind), **ConsoleLogger**, **TextFileLogger** und **XMLSerializingLogger**.

*AllowUI*

Typ: **bool**

Gibt an, ob die Überprüfungsroutine die getestete Benutzeroberfläche anzeigt. Wird in automatisierten Testszenarien im Allgemeinen auf FALSE festgelegt.

*Grafiken*

Typ: **AccCheck.GraphicsHelper**

Wird für Screenshots und andere Visualisierungen in AccChecker verwendet.

### <a name="sample-custom-verification"></a>Beispiel für benutzerdefinierte Überprüfung

Das folgende Beispiel ist eine benutzerdefinierte C#-Überprüfung, die eine einfache Tiefenüberprüfung der Elementstruktur ausführt. Ein Fehler wird protokolliert, wenn die Elementstruktur größer als 50 Ebenen ist, eine Warnung wird protokolliert, wenn die Elementstruktur 20 bis 50 Ebenen tief ist, und andernfalls wird eine Informationsmeldung protokolliert.


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
> Eine Microsoft Visual Studio Lösung, die Beispielcode für die Überprüfung enthält, ist in der Hilfedokumentation enthalten. Die Dateien befinden sich im AccChecker-Installationspfad.

 

## <a name="using-a-custom-verification"></a>Verwenden einer benutzerdefinierten Überprüfung

In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Überprüfung in AccChecker-Testszenarien integrieren.

### <a name="the-accchecker-graphical-user-interface-gui"></a>Die grafische AccChecker-Benutzeroberfläche (GUI)

Wenn Sie eine benutzerdefinierte Überprüfungsroutine in die AccChecker-Anwendung integrieren wollen, klicken Sie einfach im Menü Datei auf DLL öffnen, und suchen Sie die DLL für die Routine. Die benutzerdefinierte Routine wird am Ende der Liste der Überprüfungen im Bereich Überprüfungsroutinen auswählen hinzugefügt.

Der folgende Screenshot zeigt die benutzerdefinierte Überprüfung der Stichprobenstrukturtiefe, die AccChecker hinzugefügt wurde.

![Benutzerdefinierte Überprüfungsroutine zur Stichprobenüberprüfungsstrukturtiefe, die der Accchecker-Benutzeroberfläche hinzugefügt wurde](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Wenn die Überprüfungsattributwerte nicht in der benutzerdefinierten Überprüfungsroutine angegeben sind, wird die Überprüfung weiterhin in AccChecker geladen, obwohl sie nicht auf der Benutzeroberfläche angezeigt wird. Da sie nicht auf der Benutzeroberfläche angezeigt wird, kann sie nicht deaktiviert und von nachfolgenden Überprüfungsläufen ausgeschlossen werden.

 

### <a name="accchecker-automation"></a>AccChecker Automation

Das Integrieren einer benutzerdefinierten Überprüfungsroutine in ein automatisiertes AccChecker-Framework ist so einfach wie das Hinzufügen der Überprüfungs-DLL und das Aktivieren der gewünschten Überprüfungsroutinen.

Der folgende Codeausschnitt veranschaulicht die Verwendung der AccChecker-API zum Testen der Tabulatorfunktion in der Windows Firewall-Systemsteuerungsanwendung.


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
> Eine Microsoft Visual Studio 2008-Lösung, die Prüfbeispielcode enthält, ist in der Hilfedokumentation enthalten. Die Dateien befinden sich im AccChecker-Installationspfad.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




