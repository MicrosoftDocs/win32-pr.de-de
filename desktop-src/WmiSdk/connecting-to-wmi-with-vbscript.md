---
description: WMI-Skripts können viele der Schritte, die in einem C++-Programm erforderlich sind, zusammenfassen.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Herstellen einer Verbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866896"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Herstellen einer Verbindung mit WMI mit VBScript

WMI-Skripts können viele der Schritte, die in einem C++-Programm erforderlich sind, zusammenfassen. Sie können eine Verbindung mit WMI herstellen, nicht nur über ein " [**Swap**](swbemlocator.md) "-Objekt, sondern auch über den Moniker "winmgmts:". Ein Moniker ist ein Kurzname, der einen Namespace, eine Klasse oder eine Instanz in WMI sucht. Der Name "winmgmts:" ist der WMI-Moniker, der den Windows Script-Host anweist, die WMI-Objekte zu verwenden, eine Verbindung mit dem Standard Namespace herstellt und ein [**Swap Services**](swbemservices.md) -Objekt abruft. Andere Verbindungsinformationen (z. b. eine Identitätswechsel Ebene oder eine bestimmte Klasse oder Instanz) werden in der Zeichenfolge nach dem monikernamen angezeigt. Sie können Moniker in Aufrufen verwenden, die WMI-Objekte erstellen oder erhalten. Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md).

Im folgenden Verfahren wird beschrieben, wie mithilfe von " **Swap-Locator**" eine Verbindung mit WMI hergestellt wird.

**So stellen Sie mithilfe von "Swap Login" eine Verbindung mit WMI her**

1.  Abrufen eines Serverlocatorpunkt [-Objekts mit einem Aufrufen von "](/previous-versions//xzysf6hc(v=vs.85))"

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Melden Sie sich beim-Namespace an, indem Sie die [**ConnectServer**](swbemlocator-connectserver.md) -Methode verwenden.

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Wenn Sie im [**Anschluss an ConnectServer**](swbemlocator-connectserver.md)keinen Computer angeben, wird von WMI eine Verbindung mit dem lokalen Computer hergestellt. Wenn Sie keinen Namespace angeben, stellt WMI eine Verbindung mit dem Namespace her, der im Registrierungsschlüssel angegeben ist.

    **HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard Namespace**

    Der Standard Namespace ist \\ root \\ CIMV2. Weitere Informationen zu Namespaces finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).

3.  Legen Sie die Identitätswechsel Ebene mit einem aufzurufenden Befehl der Methode " [**Swap Services. Security \_**](swbemservices-security-.md) " fest.

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Implementieren Sie den Zweck des Skripts.

    WMI macht eine Vielzahl von Skript Objekten verfügbar, die für den Zugriff auf und die Bearbeitung von Daten in Ihrem Netzwerk verwenden. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und der [Skript-API für WMI](scripting-api-for-wmi.md).

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

    

Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit WMI hergestellt und ein Objekt mithilfe eines Monikers abgerufen wird.

**So stellen Sie eine Verbindung mit WMI her und rufen ein Objekt mithilfe eines Monikers ab**

1.  Aufrufen von [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) mit einem Moniker im Eingabeparameter.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Der-Muker enthält eine Reihe von Elementen, die Sie zum Herstellen einer Verbindung mit WMI verwenden können:

    -   "Winmgmts:" weist WSH an, [Skript-API-Objekte](scripting-api-objects.md)zu verwenden. In diesem speziellen Beispiel weiß das WSH, dass es ein-Objekt zurückgeben sollte, das das erste Win32 \_ ScheduledJob-Objekt im System beschreibt. Andere mögliche Objekte, die zurückgegeben werden können, sind ein Austausch Auflistungs-oder ein [**Swap Services**](swbemservices.md) -Objekt, je nachdem, was der Moniker beschreibt.

    -   Optional können Sie die Sicherheitsebenen für die Verbindung festlegen. Beachten Sie, dass Sie die Namen-und Kenn Wort Informationen jedoch nicht in einem Moniker festlegen können. Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).

    -   Sie können optional den Pfad zum WMI-Objekt definieren. Dies schließt entweder den lokalen Computer oder den Remote Computer, den Namespace sowie den Namen der Klasse ein. Weitere Informationen zur Verwendung des "VBScript"- [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI-Skripts finden Sie unter [Erstellen einer Instanz](creating-an-instance.md) und [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

2.  Anstatt ein einzelnes Element oder eine Auflistung abzurufen, können Sie auch das Objekt " [**Swap Services**](swbemservices.md) " (wie im vorherigen Beispiel beschrieben) abrufen. Anschließend können Sie zusätzliche Abfragen für das zurückgegebene Objekt aufzurufen.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    Im vorherigen Beispiel ist "Identitätswechsel" oder "Identitätswechsel Ebene = 3" die Standardprozess-Sicherheitsstufe. Im folgenden Beispiel ist es nicht erforderlich, diese Prozess Sicherheitsebene anzugeben, es sei denn, Sie müssen die Prozesssicherheit in **delegieren** ändern. Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellung in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
