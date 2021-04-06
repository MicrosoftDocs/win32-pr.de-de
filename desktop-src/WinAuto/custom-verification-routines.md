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
# <a name="custom-verification-routines"></a>Benutzerdefinierte Überprüfungs Routinen

In diesem Abschnitt wird beschrieben, wie eine benutzerdefinierte Überprüfungs Routine für das Tool für die Benutzeroberflächen Zugriffs Prüfung (accchecker) erstellt wird.

-   [Erstellen einer benutzerdefinierten Überprüfung](#creating-a-custom-verification)
    -   [Benutzerdefinierte Beispiel Überprüfung](#sample-custom-verification)
-   [Verwenden einer benutzerdefinierten Überprüfung](#using-a-custom-verification)
    -   [Die grafische Benutzeroberfläche der Zugriffs Prüfung (GUI)](#the-accchecker-graphical-user-interface-gui)
    -   [Accchecker-Automatisierung](#accchecker-automation)
-   [Zugehörige Themen](#related-topics)

Die UI-Barrierefreiheits Prüfung (accchecker) ist ein Tool zur Barrierefreiheit, mit dem die Implementierung von Microsoft Active Accessibility (MSAA) in einer Steuerelement-oder Anwendungs Benutzeroberfläche überprüft werden kann. Die Auswirkungen auf Barrierefreiheits Probleme, die möglicherweise durch die MSAA-Implementierung verfügbar gemacht werden, werden mit einer Reihe integrierter automatisierter Überprüfungs Routinen getestet. Diese nativen Überprüfungs Routinen können mithilfe der Extensible accchecker-Plattform durch angepasste Routinen erweitert werden.

## <a name="creating-a-custom-verification"></a>Erstellen einer benutzerdefinierten Überprüfung

Eine benutzerdefinierte Überprüfung wird als Klassenbibliothek (dll) erstellt, die eine einzelne Schnittstelle ( `IVerificationRoutine` ) mit einem Member ( `Execute` ) implementiert:


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parameter**

*HWND*

Typ: **System. IntPtr**

Das HWND des Elements, das überprüft wird.

*Protokollierung*

Typ: **acccheck. Logging. ILogger**

Die ausgewählte Protokollierungs Methode. Mögliche Typen sind **akkumulatinglogger** (von der Zugriffs Prüfung verwendet, um alle Protokolleinträge zwischenzuspeichern, bis die Überprüfungen vollständig sind), **ConsoleLogger**, **textfilelogger** und **xmlserializinglogger**.

*Zuordnung*

Typ: **bool**

Gibt an, ob die Überprüfungs Routine die zu testenden Benutzeroberfläche anzeigt. In automatisierten Testszenarien wird in der Regel auf false festgelegt.

*Grafik*

Typ: **acccheck. graphicshelper**

Wird für Screenshots und andere Visualisierungen innerhalb der accchecker verwendet.

### <a name="sample-custom-verification"></a>Benutzerdefinierte Beispiel Überprüfung

Das folgende Beispiel ist eine benutzerdefinierte c#-Überprüfung, die eine einfache Elementstruktur-tiefen Prüfung ausführt. Ein Fehler wird protokolliert, wenn die Elementstruktur größer als 50 Ebenen tief ist. eine Warnung wird protokolliert, wenn die Elementstruktur 20 bis 50 Ebenen tief ist, und andernfalls eine Informations Meldung protokolliert wird.


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
> In der Hilfe Dokumentation finden Sie eine Microsoft Visual Studio Lösung mit Überprüfungs Beispielcode. Die Dateien befinden sich im accchecker-Installationspfad.

 

## <a name="using-a-custom-verification"></a>Verwenden einer benutzerdefinierten Überprüfung

In diesem Abschnitt wird beschrieben, wie Sie eine benutzerdefinierte Überprüfung in accchecker-Testszenarien integrieren.

### <a name="the-accchecker-graphical-user-interface-gui"></a>Die grafische Benutzeroberfläche der Zugriffs Prüfung (GUI)

Wenn Sie eine benutzerdefinierte Überprüfungs Routine in die accchecker-Anwendung einschließen möchten, klicken Sie einfach im Menü Datei auf dll öffnen, und suchen Sie die DLL für die Routine. Die benutzerdefinierte Routine wird am Ende der Liste der Überprüfungen im Bereich Überprüfungs Routinen auswählen hinzugefügt.

Der folgende Screenshot zeigt die benutzerdefinierte Überprüfung der Überprüfung der Struktur Tiefe, die der Zugriffs Prüfung hinzugefügt wurde.

![Beispiel für Überprüfung der benutzerdefinierten Überprüfungs Routine für die Benutzeroberfläche der accchecker-Benutzeroberfläche](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Wenn die Überprüfungs Attributwerte nicht in der benutzerdefinierten Überprüfungs Routine angegeben werden, wird die Überprüfung weiterhin in die Zugriffs Prüfung geladen, auch wenn Sie nicht in der Benutzeroberfläche angezeigt wird. Da es nicht in der Benutzeroberfläche angezeigt wird, kann es nicht deaktiviert und von nachfolgenden Überprüfungs Läufen ausgeschlossen werden.

 

### <a name="accchecker-automation"></a>Accchecker-Automatisierung

Das Integrieren einer benutzerdefinierten Überprüfungs Routine in ein automatisiertes accchecker-Framework ist so einfach wie das Hinzufügen der Überprüfungs-dll und das Aktivieren der gewünschten Überprüfungs Routinen.

Der folgende Code Ausschnitt veranschaulicht, wie die accesschecker-API verwendet wird, um die Tabstopps-Funktionalität in der System Steuerungsanwendung der Windows-Firewall zu testen.


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
> In der Hilfe Dokumentation finden Sie eine Microsoft Visual Studio 2008-Lösung mit Überprüfungs Beispielcode. Die Dateien befinden sich im accchecker-Installationspfad.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




