---
description: Sie können eine Remoteverbindung mit WMI mit VBScript erstellen, indem Sie ein Verbindungsobjekt erstellen. Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmeldeinformationen und Authentifizierungsebenen.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Herstellen einer Remoteverbindung mit WMI mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ccdd4466273cdc3b49399abf30915a975418433183d821482a8fa92920d52d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819688"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Herstellen einer Remoteverbindung mit WMI mit VBScript

Sie können eine Remoteverbindung mit WMI mit VBScript erstellen, indem Sie ein Verbindungsobjekt erstellen. Dieses Objekt enthält den Namen des Computers, den WMI-Namespace, mit dem Sie eine Verbindung herstellen möchten, sowie alle relevanten Anmeldeinformationen und Authentifizierungsebenen.

**So stellen Sie mit VBScript eine Verbindung mit einem Remotesystem herstellen**

1.  Geben Sie die Verbindungsinformationen an, z. B. den Namen des Remotecomputers, die Anmeldeinformationen und die Authentifizierungsebene für die Verbindung.

    Wenn Sie eine Verbindung mit einem Remotecomputer mit den gleichen Anmeldeinformationen (Domäne und Benutzername) herstellen, mit dem Sie angemeldet sind, können Sie die Verbindungsinformationen in einem [**GetObject-Moniker**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[](constructing-a-moniker-string.md)angeben, wie im folgenden Codebeispiel beschrieben.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    Im Allgemeinen sollten Sie den WMI-Namespace angeben, mit dem auf dem Remotecomputer eine Verbindung hergestellt werden soll. Dies liegt daran, dass es möglich ist, dass der Standardnamespace auf verschiedenen Computern nicht identisch ist. Wenn Sie den Namespace angeben, stellen Sie sicher, dass Sie auf allen Computern eine Verbindung mit demselben Namespace herstellen.

    Weitere Informationen zu VBScript-Konstanten und Skriptzeichenfolgen für die Verwendung der Monikerverbindung finden Sie unter [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Wenn Sie eine Verbindung mit einem Remotecomputer in einer anderen Domäne herstellen oder einen anderen Benutzernamen und ein anderes Kennwort verwenden, müssen Sie die [**SWbemLocator.ConnectServer-Methode**](swbemlocator-connectserver.md) verwenden.

    Wie bei einem Moniker verwenden Sie **ConnectServer,** um die Anmeldeinformationen, die Authentifizierungsebene und den Namespace für die Remoteverbindung anzugeben. Im folgenden Codebeispiel wird die Verwendung von ConnectServer für den Zugriff auf einen Remotecomputer mithilfe eines Administratorkontos und Kennworts beschrieben.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Wenn Sie die [**ConnectServer-Funktion**](swbemlocator-connectserver.md) für Remoteverbindungen verwenden, legen Sie den Identitätswechsel und die Authentifizierung für das Sicherheitsobjekt fest, das durch einen Aufruf von [**SWbemServices.Security erhalten wurde.**](swbemservices-security-.md) Sie können die Enumeration [WbemImpersonationLevelEnum verwenden,](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) um die Identitätswechselebene anzugeben.

    Das folgende Codebeispiel legt die Identitätswechselebene für das vorherige VBScript-Codebeispiel fest.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Beachten Sie, dass einige Verbindungen eine bestimmte Authentifizierungsebene erfordern. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md) und [Securing Scripting Clients](securing-scripting-clients.md).

    Insbesondere sollten Sie die Authentifizierungsebene auf **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** oder 6 festlegen, wenn für den Namespace, mit dem Sie eine Verbindung auf dem Remotecomputer herstellen, eine verschlüsselte Verbindung erforderlich ist, bevor Daten zurückgeben werden. Sie können diese Authentifizierungsebene auch dann verwenden, wenn der Namespace sie nicht benötigt. Dadurch wird sichergestellt, dass Daten verschlüsselt werden, wenn sie das Netzwerk überqueren. Wenn Sie versuchen, eine niedrigere Authentifizierungsebene als zulässig zu setzen, wird eine Meldung zu verweigerten Zugriffen zurückgegeben. Weitere Informationen finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

Nachdem Sie die Verbindung hergestellt haben, können Sie weiterhin auf WMI-Daten zugreifen. Weitere Informationen finden Sie unter WMI Tasks for Scripts and Applications ( [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)).

## <a name="examples"></a>Beispiele

Ein größeres VBScript-Beispiel finden Sie im Abschnitt Beispiele auf der [**Referenzseite zu SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md)

The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer. Zum Ausführen des folgenden Skripts müssen Sie Administrator auf den Remotecomputern sein. Beachten Sie, dass " " erforderlich ist, bevor der Name des Remotecomputers vom Skript nach der Einstellung für die \\ \\ Identitätswechselebene hinzugefügt wird. Weitere Informationen zu WMI-Pfaden finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)


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



Im folgenden VBScript-Codebeispiel können Sie mithilfe verschiedener Anmeldeinformationen eine Verbindung mit einem Remotecomputer herstellen. Beispielsweise ein Remotecomputer in einer anderen Domäne oder das Herstellen einer Verbindung mit einem Remotecomputer, der einen anderen Benutzernamen und ein anderes Kennwort erfordert. Verwenden Sie in diesem Fall die [**SWbemServices.ConnectServer-Verbindung.**](swbemlocator-connectserver.md)


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

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
