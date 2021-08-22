---
description: WMI-Skripts können viele der schritte, die in einem C++-Programm erforderlich sind, verdichten.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Herstellen einer Verbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b4e71f4225a55e24432562d4c35754080b9746386489b7dbf7061cb65c9771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131612"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Herstellen einer Verbindung mit WMI mit VBScript

WMI-Skripts können viele der schritte, die in einem C++-Programm erforderlich sind, verdichten. Sie können nicht nur über ein [**SWbemLocator-Objekt,**](swbemlocator.md) sondern auch über den Moniker "winmgmts:" eine Verbindung mit WMI herstellen. Ein Moniker ist ein Kurzname, der einen Namespace, eine Klasse oder eine Instanz in WMI sucht. Der Name "winmgmts:" ist der WMI-Moniker, der den Windows-Skripthost an weist, die WMI-Objekte zu verwenden, eine Verbindung mit dem Standardnamespace herstellt und ein [**SWbemServices-Objekt erhält.**](swbemservices.md) Andere Verbindungsinformationen, z. B. eine Identitätswechselebene oder eine bestimmte Klasse oder Instanz, werden in der Zeichenfolge nach dem Monikernamen angezeigt. Sie können Moniker in Aufrufen verwenden, die WMI-Objekte erstellen oder erhalten. Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge.](constructing-a-moniker-string.md)

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von **SWbemLocator** eine Verbindung mit WMI herstellen.

**So stellen Sie mithilfe von SWbemLocator eine Verbindung mit WMI her**

1.  Rufen Sie ein Locatorobjekt mit einem Aufruf von [CreateObject ab.](/previous-versions//xzysf6hc(v=vs.85))

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Melden Sie sich mithilfe eines Aufrufs der [**ConnectServer-Methode beim Namespace**](swbemlocator-connectserver.md) an.

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Wenn Sie im Aufruf von [**ConnectServer**](swbemlocator-connectserver.md)keinen Computer angeben, stellt WMI eine Verbindung mit dem lokalen Computer her. Wenn Sie keinen Namespace angeben, stellt WMI eine Verbindung mit dem im Registrierungsschlüssel angegebenen Namespace her.

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** Scripting \\ **Default** \\ **Namespace**

    Der Standardnamespace ist \\ \\ "root cimv2". Weitere Informationen zu Namespaces finden Sie unter [Erstellen von Hierarchien in WMI.](creating-hierarchies-within-wmi.md)

3.  Legen Sie die Identitätswechselebene mit einem Aufruf der [**SWbemServices.Security-Methode \_**](swbemservices-security-.md) fest.

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Implementieren Sie den Zweck Ihres Skripts.

    WMI macht eine Vielzahl von Skriptobjekten verfügbar, die verwenden, um auf Daten in Ihrem Netzwerk zu zugreifen und diese zu bearbeiten. Weitere Informationen finden Sie unter [Manipulating Class and Instance Information (Bearbeiten von Klassen- und Instanzinformationen)](manipulating-class-and-instance-information.md) und [Scripting API for WMI (Skripterstellungs-API für WMI).](scripting-api-for-wmi.md)

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine Verbindung mit WMI herstellen und ein Objekt mithilfe eines Monikers abrufen.

**So stellen Sie eine Verbindung mit WMI her und rufen ein Objekt mithilfe eines Monikers ab**

1.  Rufen [**Sie GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) mit einem Moniker im Eingabeparameter auf.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Der Moiniker enthält eine Reihe von Elementen, mit denen Sie eine Verbindung mit WMI herstellen können:

    -   "winmgmts:" weist WSH an, [Skripterstellungs-API-Objekte zu verwenden.](scripting-api-objects.md) In diesem speziellen Beispiel weiß die WSH, dass sie ein SWbemObject zurückgeben sollte, das den ersten win32 scheduledJob im \_ System beschreibt. Andere mögliche Objekte, die zurückgeben werden können, sind eine SWbemCollection oder ein [**SWbemServices-Objekt,**](swbemservices.md) je nachdem, was der Moniker beschrieben hat.

    -   Optional können Sie die Sicherheitsebenen für die Verbindung festlegen. Beachten Sie jedoch, dass Sie keine Namens- und Kennwortinformationen in einem Moniker festlegen können. Weitere Informationen finden Sie unter [Schützen von Skriptclients.](securing-scripting-clients.md)

    -   Optional können Sie den Pfad zum WMI-Objekt definieren. Dies schließt entweder den lokalen oder Remotecomputer, den Namespace sowie den Namen der Klasse ein. Weitere Informationen zur Verwendung von VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI-Skripts finden Sie unter [Erstellen](creating-an-instance.md) einer Instanz und Abrufen [einer WMI-Instanz.](retrieving-an-instance.md)

2.  Anstatt ein einzelnes Element oder eine Sammlung abzurufen, können Sie auch das [**SWbemServices-Objekt**](swbemservices.md) abrufen (wie im vorherigen Beispiel beschrieben). Anschließend können Sie zusätzliche Abfragen für das zurückgegebene Objekt aufrufen.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    Im vorherigen Beispiel ist impersonate oder impersonationLevel=3 die Standardprozesssicherheitsebene. Im folgenden Beispiel ist es nicht erforderlich, diese Prozesssicherheitsstufe anzugeben, es sei denn, Sie müssen die Prozesssicherheit ändern, um **zu delegieren.** Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mit VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
