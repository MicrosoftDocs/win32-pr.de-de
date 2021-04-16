---
title: Benutzeroberflächenautomatisierungs-Test Bibliothek
description: Die UI Automation-Test Bibliothek (UIA Test Library) ist eine API, die von der Treiber Anwendung in einem automatisierten Testszenario aufgerufen wird.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104557280"
---
# <a name="ui-automation-test-library"></a>Benutzeroberflächenautomatisierungs-Test Bibliothek

Die UI Automation-Test Bibliothek (UIA Test Library) ist eine API, die von der *Treiber* Anwendung in einem automatisierten Testszenario aufgerufen wird. Der Treiber ist die Anwendung, die ein Automation-Element ([**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekt) aus einem Steuerelement abruft, das überprüft werden muss, und es für die UI Automation-Test Bibliothek bereitstellt. Die Test Bibliothek überprüft und überprüft dann die Implementierung der Benutzeroberflächen Automatisierung. Weitere Informationen zu Benutzeroberflächenautomatisierungs-und Automatisierungs Elementen finden Sie Untergrund lagen zur Automatisierung der [Benutzeroberfläche](entry-uiautocore-overview.md).

-   [Workflow für UI-Automatisierungs-Test Bibliothek](#ui-automation-test-library-workflow)
-   [Protokollierung mit der Benutzeroberflächenautomatisierungs-Test Bibliothek](#logging-with-the-ui-automation-test-library)
    -   [XML-Protokollierung](#xml-logging)
    -   [Konsolen Protokollierung](#console-logging)
    -   [Code Anforderungen für die Protokollierung](#code-requirements-for-logging)
    -   [Protokollierungs Beispiele](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Workflow für UI-Automatisierungs-Test Bibliothek

Das folgende Diagramm zeigt einen Test Workflow, der die Benutzeroberflächenautomatisierungs-Test Bibliothek mithilfe einer Konsolenanwendung als Treiber enthält. In diesem Fall startet der Treiber eine Instanz von Notepad.exe und erhält ein Automation-Element (d. h. ein [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekt) aus dem Bearbeitungs Steuerelement. Als Nächstes erstellt der Treiber ein UI-Automatisierungs-Test Bibliotheksobjekt basierend auf der UI-Plattform, die getestet wird, und übergibt dann das Automation-Element als Parameter. Die Benutzeroberflächenautomatisierungs-Test Bibliothek bestimmt, dass das Automation-Element ein [Dokument](uiauto-supportdocumentcontroltype.md) Steuerungstyp ist, und führt dann die Dokument Steuerungs Tests, die Muster Tests für [Text](uiauto-implementingtextandtextrange.md) -und Bild Lauf Steuer [Elemente sowie generische](uiauto-implementingscroll.md) Automatisierungs Element Tests aus.

![Diagramm, das den Fluss des Treibers zu einer Anwendung zu einem Treiber an uiatestlibrary mithilfe von roten Pfeilen anzeigt.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Protokollierung mit der Benutzeroberflächenautomatisierungs-Test Bibliothek

Die UI Automation-Test Bibliothek verwendet externe DLLs, um Ergebnisse aus Test Läufen zu protokollieren. Es unterstützt die Protokollierung als XML und die Protokollierung auf der Konsole.

### <a name="xml-logging"></a>XML-Protokollierung

Die XML-Protokollierung wird in der Regel von der Überprüfung der visuellen Benutzeroberflächen Automatisierung verwendet, kann aber auch in einen Befehlszeilen Workflow integriert werden.

Wenn die XML-Protokollierung angegeben ist, muss die Treiber Anwendung die Ausgabe serialisieren, indem Sie ein **XmlWriter** -Objekt erstellt und an die **xmllog. gettestrauunxml** -Methode übergibt. Der Treiber kann dann den serialisierten XML-Code intern verwenden oder in eine Datei schreiben.

Die folgenden DLLs sind für die XML-Protokollierung erforderlich.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Konsolen Protokollierung

Standardmäßig verwendet die UI Automation-Test Bibliothek die Konsolen Protokollierung, bei der die gesamte Protokollierungs Ausgabe als nur-Text an das Konsolenfenster weitergeleitet wird. WUIALogging.dll ist für die Konsolen Protokollierung erforderlich.

### <a name="code-requirements-for-logging"></a>Code Anforderungen für die Protokollierung

Eine Treiber Anwendung muss die folgenden Code Ausschnitte zur Verwendung der Benutzeroberflächenautomatisierungs-Test Bibliotheks Protokollierung enthalten.


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a>Protokollierungs Beispiele

In den folgenden Beispielen wird die grundlegende Protokollierungs Funktionalität veranschaulicht, und es wird gezeigt, wie Sie die UI Automation-Test Bibliotheks-API in einer grundlegenden Test Automatisierungs Treiber


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




