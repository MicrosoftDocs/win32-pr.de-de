---
description: Sie können eine Remote Verbindung mit WMI mit VBScript herstellen, indem Sie ein Verbindungs Objekt erstellen. Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmelde Informationen und Authentifizierungs Ebenen.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Remote Verbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345276"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Remote Verbindung mit WMI mit VBScript

Sie können eine Remote Verbindung mit WMI mit VBScript herstellen, indem Sie ein Verbindungs Objekt erstellen. Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmelde Informationen und Authentifizierungs Ebenen.

**So stellen Sie eine Verbindung mit einem Remote System mithilfe von VBScript her**

1.  Geben Sie die Verbindungsinformationen an, z. b. den Remote Computernamen, die Anmelde Informationen und die Authentifizierungs Ebene für die Verbindung.

    Wenn Sie mit den gleichen Anmelde Informationen (Domäne und Benutzername), mit denen Sie angemeldet sind, eine Verbindung mit einem Remote Computer herstellen, können Sie die Verbindungsinformationen in einem [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)-[Moniker](constructing-a-moniker-string.md)angeben, wie im folgenden Codebeispiel beschrieben.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    Im Allgemeinen sollten Sie den WMI-Namespace angeben, mit dem auf dem Remote Computer eine Verbindung hergestellt werden soll. Dies liegt daran, dass es möglich ist, dass der Standard Namespace auf unterschiedlichen Computern nicht identisch ist. Durch die Angabe des Namespace wird sichergestellt, dass Sie eine Verbindung mit dem gleichen Namespace auf allen Computern herstellen.

    Weitere Informationen zu VBScript-Konstanten und Skript Zeichenfolgen für die Verwendung der monikerverbindung finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Wenn Sie eine Verbindung mit einem Remote Computer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie die Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " verwenden.

    Wie bei einem Moniker verwenden Sie **ConnectServer** , um die Anmelde Informationen, die Authentifizierungs Ebene und den Namespace für die Remote Verbindung anzugeben. Im folgenden Codebeispiel wird die Verwendung von ConnectServer für den Zugriff auf einen Remote Computer mithilfe eines Administrator Kontos und Kennworts beschrieben.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Wenn Sie die [**ConnectServer**](swbemlocator-connectserver.md) -Funktion für Remote Verbindungen verwenden, legen Sie Identitätswechsel und Authentifizierung für das Sicherheits Objekt fest, das durch einen aufrufswert von " [**Swap Services. Security**](swbemservices-security-.md)" abgerufen wird Sie können die Enumeration [wbemimpersonationlevelenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) zum Angeben der Identitätswechsel Ebene verwenden.

    Im folgenden Codebeispiel wird die Identitätswechsel Ebene für das vorherige VBScript-Codebeispiel festgelegt.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Beachten Sie, dass einige Verbindungen eine bestimmte Authentifizierungs Ebene erfordern. Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md) und [Sichern von Skript Clients](securing-scripting-clients.md).

    Insbesondere sollten Sie die Authentifizierungs Ebene auf **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** oder 6 festlegen, wenn der Namespace, für den Sie eine Verbindung mit dem Remote Computer herstellen, eine verschlüsselte Verbindung erfordert, bevor Daten zurückgegeben werden. Sie können diese Authentifizierungs Ebene auch dann verwenden, wenn Sie vom Namespace nicht benötigt wird. Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden. Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, als zulässig ist, wird die Meldung "Zugriff verweigert" zurückgegeben. Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Nachdem Sie die Verbindung hergestellt haben, können Sie weiterhin auf WMI-Daten zugreifen. Weitere Informationen finden Sie unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md).

## <a name="examples"></a>Beispiele

Ein umfangreicheres VBScript-Beispiel finden Sie im Abschnitt "Beispiele" auf der Referenzseite zu " [**mpbemlocator. ConnectServer**](swbemlocator-connectserver.md) ".

Im folgenden VBScript-Codebeispiel wird eine Verbindung mit einer Gruppe von Remote Computern in derselben Domäne hergestellt, indem ein Array von Remote Computernamen erstellt und dann die Namen der Plug & Play Geräte – Instanzen von [**Win32 \_ pnptity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)– auf den einzelnen Computern angezeigt werden. Zum Ausführen des folgenden Skripts müssen Sie Administrator auf den Remote Computern sein. Beachten Sie, dass \\ \\ vor dem Hinzufügen des Remote Computer namens durch das Skript nach der Einstellung der Identitätswechsel Ebene "" erforderlich ist. Weitere Informationen zu WMI-Pfaden finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



Mithilfe des folgenden VBScript-Code Beispiels können Sie eine Verbindung mit einem Remote Computer mithilfe verschiedener Anmelde Informationen herstellen. Beispielsweise ein Remote Computer in einer anderen Domäne oder eine Verbindung mit einem Remote Computer, der einen anderen Benutzernamen und ein anderes Kennwort benötigt. Verwenden Sie in diesem Fall die Verbindung " [**Swap Services. ConnectServer**](swbemlocator-connectserver.md) ".


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
