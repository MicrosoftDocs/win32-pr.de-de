---
description: Stellt eine Verbindung mit dem Namespace auf dem Computer her, der im strServer-Parameter angegeben ist.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: SWbemLocator.ConnectServer-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4153a5761d59c54cf8635202adcca0ddf72603022ebf8dbb5b160231c90e49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955210"
---
# <a name="swbemlocatorconnectserver-method"></a>SWbemLocator.ConnectServer-Methode

Die **ConnectServer-Methode** des [**SWbemLocator-Objekts**](swbemlocator.md) stellt eine Verbindung mit dem Namespace auf dem Computer her, der im *strServer-Parameter* angegeben ist. Der Zielcomputer kann entweder lokal oder remote sein, aber WMI muss installiert sein. Beispiele und einen Vergleich mit dem Monikertyp der Verbindung finden Sie unter [Erstellen eines WMI-Skripts.](creating-a-wmi-script.md)

Ab Windows Vista kann **SWbemLocator.ConnectServer** über eine IPv6-Adresse im *strServer-Parameter* eine Verbindung mit Computern herstellen, auf denen IPv6 ausgeführt wird. Weitere Informationen finden Sie unter [IPv6- und IPv4-Unterstützung in WMI.](ipv6-and-ipv4-support-in-wmi.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strServer* \[ in, optional\]
</dt> <dd>

Computername, mit dem Sie eine Verbindung herstellen. Wenn sich der Remotecomputer in einer anderen Domäne als das Benutzerkonto befindet, unter dem Sie sich anmelden, verwenden Sie den vollqualifizierten Computernamen. Wenn Sie diesen Parameter nicht angeben, wird standardmäßig der lokale Computer aufgerufen.

Beispiel: `server1.network.fabrikam`

Sie können auch eine IP-Adresse in diesem Parameter verwenden. Wenn die IP-Adresse im IPv6-Format vorliegt, muss auf dem Zielcomputer IPv6 ausgeführt werden. Eine Adresse in IPv4 sieht wie folgt aus: `123.123.123.123`

Eine IP-Adresse im IPv6-Format sieht wie folgt aus: `2010:836B:4179::836B:4179`

Weitere Informationen zu DNS und IPv4 finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*strNamespace* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die den Namespace angibt, bei dem Sie sich anmelden. Wenn Sie sich beispielsweise beim \\ Stammstandardnamespace anmelden möchten, verwenden Sie root \\ default. Wenn Sie diesen Parameter nicht angeben, wird standardmäßig der Namespace verwendet, der als Standardnamespace für die Skripterstellung konfiguriert ist. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts.](creating-a-wmi-application-or-script.md)

Beispiel: "root \\ CIMV2"

</dd> <dt>

*strUser* \[ in, optional\]
</dt> <dd>

Benutzername, der zum Herstellen der Verbindung verwendet werden soll. Die Zeichenfolge kann entweder in Form eines Benutzernamens oder eines \\ Domänenbenutzernamens verwendet werden. Lassen Sie diesen Parameter leer, um den aktuellen Sicherheitskontext zu verwenden. Der *strUser-Parameter* sollte nur mit Verbindungen mit WMI-Remoteservern verwendet werden. Wenn Sie versuchen, *strUser* für eine lokale WMI-Verbindung anzugeben, schlägt der Verbindungsversuch fehl. Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in *strUser* und *strPassword* angegeben sind, nicht in einem Netzwerk abgefangen werden. Sie können das UPN-Format verwenden, um *strUser* anzugeben.

Beispiel: "DomainName \\ UserName"

> [!Note]  
> Wenn eine Domäne in *strAuthority* angegeben ist, darf die Domäne hier nicht angegeben werden. Das Angeben der Domäne in beiden Parametern führt zu einem Fehler aufgrund eines ungültigen Parameters.

 

</dd> <dt>

*strPassword* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die das Kennwort angibt, das beim Verbindungsversuch verwendet werden soll. Lassen Sie den Parameter leer, um den aktuellen Sicherheitskontext zu verwenden. Der *parameter strPassword* sollte nur mit Verbindungen mit WMI-Remoteservern verwendet werden. Wenn Sie versuchen, *strPassword* für eine lokale WMI-Verbindung anzugeben, schlägt der Verbindungsversuch fehl. Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in *strUser* und *strPassword* angegeben sind, nicht im Netzwerk abgefangen werden.

</dd> <dt>

*strLocale* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die den Lokalisierungscode angibt. Wenn Sie das aktuelle Gebietsschema verwenden möchten, lassen Sie es leer. Wenn er nicht leer ist, muss dieser Parameter eine Zeichenfolge sein, die das gewünschte Gebietsschema angibt, in dem Informationen abgerufen werden müssen. Für Microsoft-Gebietsschemabezeichner lautet das Format der Zeichenfolge "MS \_ xxxx", wobei xxxx eine Zeichenfolge im hexadezimalen Format ist, die die LCID angibt. Beispielsweise würde amerikanisches Englisch als "MS \_ 409" angezeigt.

</dd> <dt>

*strAuthority* \[ in, optional\]
</dt> <dd>

<dt>

""
</dt> <dd>

Dieser Parameter ist optional. Wenn sie jedoch angegeben ist, können nur Kerberos oder NTLMDomain verwendet werden.

</dd> <dt>

Kerberos:
</dt> <dd>

Wenn der *strAuthority-Parameter* mit der Zeichenfolge "Kerberos:" beginnt, wird die Kerberos-Authentifizierung verwendet, und dieser Parameter sollte einen Kerberos-Prinzipalnamen enthalten. Der Kerberos-Prinzipalname wird als Kerberos:*Domäne* angegeben, z. `Kerberos:fabrikam` B. wobei `fabrikam` der Server ist, mit dem Sie eine Verbindung herstellen möchten.

Beispiel: "Kerberos:DOMAIN"

</dd> <dt>

NTLMDomain:
</dt> <dd>

Um die NTLM-Authentifizierung (NT Lan Manager) zu verwenden, müssen Sie sie als NTLMDomain:*Domäne* angeben, z. B. `NTLMDomain:fabrikam` wobei der Name der Domäne `fabrikam` ist.

Beispiel: "NTLMDomain:DOMAIN"

</dd> </dl>

Wenn Sie diesen Parameter leer lassen, handelt das Betriebssystem mit COM aus, um zu bestimmen, ob die NTLM- oder Kerberos-Authentifizierung verwendet wird. Dieser Parameter sollte nur mit Verbindungen mit WMI-Remoteservern verwendet werden. Wenn Sie versuchen, die Autorität für eine lokale WMI-Verbindung festzulegen, schlägt der Verbindungsversuch fehl.

> [!Note]  
> Wenn die Domäne in *strUser* angegeben ist, was der bevorzugte Speicherort ist, darf sie hier nicht angegeben werden. Das Angeben der Domäne in beiden Parametern führt zu einem Fehler aufgrund eines ungültigen Parameters.

 

</dd> <dt>

*iSecurityFlags* \[ in, optional\]
</dt> <dd>

Wird verwendet, um Flagwerte an **ConnectServer** zu übergeben.

<dt>

0 (0x0)
</dt> <dd>

Der Wert 0 für diesen Parameter bewirkt, dass der Aufruf von **ConnectServer** erst zurückgegeben wird, nachdem die Verbindung mit dem Server hergestellt wurde. Dies kann dazu führen, dass Ihr Programm nicht mehr unbegrenzt reagiert, wenn die Verbindung nicht hergestellt werden kann.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait® (128 (0x80))


</dt> <dd>

Der **ConnectServer-Aufruf** gibt garantiert in 2 Minuten oder weniger zurück. Verwenden Sie dieses Flag, um zu verhindern, dass Ihr Programm auf unbestimmte Zeit reagiert, wenn die Verbindung nicht hergestellt werden kann.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt WMI ein [**SWbemServices-Objekt**](swbemservices.md) zurück, das an den Namespace gebunden ist, der in *strNamespace* auf dem Computer angegeben ist, der in *strServer* angegeben ist.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ConnectServer-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle oder angegebene Benutzername und das angegebene Kennwort waren nicht gültig oder zum Herstellen der Verbindung autorisiert.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidNamespace** – 2147749902 (0x8004100E)
</dt> <dd>

Der angegebene Namespace war auf dem Server nicht vorhanden.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein ungültiger Parameter wurde angegeben, oder der Namespace konnte nicht analysiert werden.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrTransportFailure** – 2147749909
</dt> <dd>

Es ist ein Netzwerkfehler aufgetreten, der den normalen Betrieb verhindert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ConnectServer-Methode** wird häufig verwendet, wenn eine Verbindung mit einem Konto mit einem anderen Benutzernamen und anderen Kennwortanmeldeinformationen auf einem Remotecomputer hergestellt wird, da Sie kein anderes Kennwort in einer [Monikerzeichenfolge](constructing-a-moniker-string.md) angeben können. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

Die Verwendung einer IPv4-Adresse zum Herstellen einer Verbindung mit einem Remoteserver kann zu unerwartetem Verhalten führen. Die wahrscheinliche Ursache sind veraltete DNS-Einträge in Ihrer Umgebung. Unter diesen Umständen wird der veraltete PTR-Eintrag für den Computer mit unvorhersehbaren Ergebnissen verwendet. Um dieses Verhalten zu vermeiden, können Sie einen Punkt (".") an die IP-Adresse anfügen, bevor Sie ConnectServer aufrufen. Dies führt dazu, dass die Reverse-DNS-Suche fehlschlägt, der **ConnectServer-Aufruf** jedoch möglicherweise auf dem richtigen Computer erfolgreich ist.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird beschrieben, wie Sie eine Verbindung mit einem Remotecomputer herstellen, um [**Win32 \_ IP4RouteTable-Daten zu**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) erhalten. Der in *strDomain* angegebene Domänenname wird in *strAuthority verwendet.*


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



Der folgende PowerShell-Codeausschnitt greifen auf einen Remoteserver zu und listet die verfügbaren WMI-Klassen auf.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> </dl>

 

