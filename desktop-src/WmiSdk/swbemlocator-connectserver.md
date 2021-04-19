---
description: Stellt eine Verbindung mit dem Namespace auf dem Computer her, der im Parameter "strinserver" angegeben ist.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Methode "Swap. ConnectServer" (wbemdisp. h)
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
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369835"
---
# <a name="swbemlocatorconnectserver-method"></a>Methode "Swap. ConnectServer"

Die **ConnectServer** -Methode des Objekts " [**Swap-Locator**](swbemlocator.md) " stellt eine Verbindung mit dem Namespace auf dem Computer her, der im Parameter " *strinserver* " angegeben ist. Der Zielcomputer kann entweder lokal oder Remote sein, aber es muss WMI installiert sein. Beispiele und einen Vergleich mit dem monikertyp Verbindung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).

Ab Windows Vista kann der **Austausch von "taubemlocator. ConnectServer** " mit Computern, auf denen IPv6 ausgeführt wird, über eine IPv6-Adresse *im Parameter "* Parameter" verwendet werden. Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

- *Server* \[ in, optional\]
</dt> <dd>

Der Name des Computers, mit dem Sie eine Verbindung herstellen. Wenn sich der Remote Computer in einer anderen Domäne als das Benutzerkonto befindet, unter dem Sie sich anmelden, verwenden Sie den voll qualifizierten Computernamen. Wenn Sie diesen Parameter nicht angeben, wird als Standardwert der lokale Computer verwendet.

Ein Beispiel: `server1.network.fabrikam`

Sie können auch eine IP-Adresse in diesem Parameter verwenden. Wenn die IP-Adresse im IPv6-Format vorliegt, muss auf dem Bereitstellungs Zielcomputer IPv6 ausgeführt werden. Eine Adresse in IPv4 sieht wie folgt aus. `123.123.123.123`

Eine IP-Adresse im IPv6-Format sieht wie folgt aus `2010:836B:4179::836B:4179`

Weitere Informationen zu DNS und IPv4 finden Sie im Abschnitt "Hinweise".

</dd> <dt>

" *strinnamespace* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Namespace angibt, an dem Sie sich anmelden. Wenn Sie sich beispielsweise beim Stamm- \\ Standard Namespace anmelden möchten, verwenden Sie root \\ default. Wenn Sie diesen Parameter nicht angeben, wird standardmäßig der Namespace verwendet, der als Standard Namespace für die Skripterstellung konfiguriert ist. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).

Beispiel: "root \\ CIMV2"

</dd> <dt>

*strUser* \[ in, optional\]
</dt> <dd>

Der zum Herstellen der Verbindung zu verwendende Benutzername. Die Zeichenfolge kann entweder einen Benutzernamen oder einen Domänen \\ Benutzernamen aufweisen. Lassen Sie diesen Parameter leer, um den aktuellen Sicherheitskontext zu verwenden. Der *strUser* -Parameter sollte nur mit Verbindungen mit Remote-WMI-Servern verwendet werden. Wenn Sie den *strUser* für eine lokale WMI-Verbindung angeben möchten, schlägt der Verbindungsversuch fehl. Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in " *strUser* " und " *stranpassword* " angegeben sind, nicht in einem Netzwerk abgefangen werden. Sie können das UPN-Format verwenden, um den *strUser* anzugeben.

Beispiel: "Domainname \\ username"

> [!Note]  
> Wenn eine Domäne in " *stranauthority*" angegeben ist, darf die Domäne hier nicht angegeben werden. Wenn Sie die Domäne in beiden Parametern angeben, führt dies zu einem ungültigen Parameter Fehler.

 

</dd> <dt>

*"Straume"* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das Kennwort angibt, das beim Verbindungsversuch verwendet werden soll. Lassen Sie den-Parameter leer, um den aktuellen Sicherheitskontext zu verwenden. Der Parameter " *straupassword* " sollte nur mit Verbindungen mit Remote-WMI-Servern verwendet werden. Wenn *Sie angeben,* dass für eine lokale WMI-Verbindung "für eine lokale WMI"-Verbindung festgelegt werden soll Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in " *strUser* " und " *stranpassword* " angegeben sind, im Netzwerk nicht abgefangen werden.

</dd> <dt>

*"Straume"* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Lokalisierungs Code angibt. Wenn Sie das aktuelle Gebiets Schema verwenden möchten, lassen Sie es leer. Wenn nicht leer, muss dieser Parameter eine Zeichenfolge sein, die das gewünschte Gebiets Schema angibt, in das Informationen abgerufen werden müssen. Für Microsoft-Gebiets Schema Bezeichner ist das Format der Zeichenfolge "MS \_ xxxx", wobei xxxx eine Zeichenfolge im Hexadezimal Format ist, die die LCID angibt. Beispielsweise würde American English als "MS \_ 409" angezeigt werden.

</dd> <dt>

- *Autorität* \[ in, optional\]
</dt> <dd>

<dt>

""
</dt> <dd>

Dieser Parameter ist optional. Wenn Sie jedoch angegeben ist, kann nur Kerberos oder ntlmdomain verwendet werden.

</dd> <dt>

Kerberos
</dt> <dd>

Wenn der Parameter " *strauauthority* " mit der Zeichenfolge "Kerberos:" beginnt, wird die Kerberos-Authentifizierung verwendet, und dieser Parameter sollte einen Kerberos-Prinzipal Namen enthalten. Der Kerberos-Prinzipal Name wird als Kerberos:*Domäne* angegeben, z `Kerberos:fabrikam` . b. Wenn `fabrikam` der Server ist, zu dem eine Verbindung hergestellt werden soll.

Beispiel: "Kerberos: Domäne"

</dd> <dt>

Quot ntlmdomain
</dt> <dd>

Um die NTLM-Authentifizierung (NT LAN Manager) verwenden zu können, müssen Sie diese als ntlmdomain:*Domain* angeben, z `NTLMDomain:fabrikam` . b `fabrikam` . wobei der Name der Domäne ist.

Beispiel: "ntlmdomain: Domain"

</dd> </dl>

Wenn Sie diesen Parameter leer lassen, verhandelt das Betriebssystem mit com, um zu bestimmen, ob die NTLM-oder Kerberos-Authentifizierung verwendet wird. Dieser Parameter sollte nur für Verbindungen mit Remote-WMI-Servern verwendet werden. Wenn Sie versuchen, die Autorität für eine lokale WMI-Verbindung festzulegen, schlägt der Verbindungsversuch fehl.

> [!Note]  
> Wenn die Domäne in " *strUser*" angegeben ist, was der bevorzugte Speicherort ist, darf Sie hier nicht angegeben werden. Wenn Sie die Domäne in beiden Parametern angeben, führt dies zu einem ungültigen Parameter Fehler.

 

</dd> <dt>

*isecurityflags* \[ in, optional\]
</dt> <dd>

Wird verwendet, um Flagwerte an **ConnectServer** zu übergeben.

<dt>

0 (0x0)
</dt> <dd>

Der Wert 0 für diesen Parameter bewirkt, dass der Connector **ConnectServer** erst nach dem Herstellen der Verbindung mit dem Server zurückgegeben wird. Dies könnte dazu führen, dass das Programm nicht mehr unbegrenzt reagiert, wenn die Verbindung nicht hergestellt werden kann.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemconnectflagusemaxwait * * * * (128 (0x80))


</dt> <dd>

Der **ConnectServer** -Rückruf wird garantiert in maximal 2 Minuten zurückgegeben. Verwenden Sie dieses Flag, um zu verhindern, dass das Programm unbegrenzt reagiert, wenn die Verbindung nicht hergestellt werden kann.

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt WMI ein-Objekt zurück, [**das an den**](swbemservices.md) Namespace gebunden ist, der auf dem in " *strinserver*" angegebenen Computer in " *strinnamespace* " angegeben ist.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ConnectServer** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle oder der angegebene Benutzername und das Kennwort waren ungültig oder zum Herstellen der Verbindung autorisiert.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100e)
</dt> <dd>

Der angegebene Namespace war auf dem Server nicht vorhanden.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben, oder der Namespace konnte nicht analysiert werden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

Netzwerkfehler. der normale Betrieb wird verhindert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **ConnectServer** -Methode wird häufig verwendet, wenn eine Verbindung mit einem Konto mit einem anderen Benutzernamen und Kenn Wort Anmelde Informationen auf einem Remote Computer hergestellt wird, da Sie kein anderes Kennwort in einer [Monikerzeichenfolge](constructing-a-moniker-string.md) angeben können. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

Das Verwenden einer IPv4-Adresse für die Verbindung mit einem Remote Server kann zu unerwartetem Verhalten führen. Die wahrscheinlichste Ursache ist ein veralteter DNS-Eintrag in Ihrer Umgebung. In diesen Fällen wird der veraltete PTR-Eintrag für den Computer mit unvorhersehbaren Ergebnissen verwendet. Um dieses Verhalten zu vermeiden, können Sie vor dem Aufrufen von ConnectServer einen Punkt (".") an die IP-Adresse anfügen. Dies bewirkt, dass bei der Reverse-DNS-Suche ein Fehler auftritt, der **Verbindungs Server** jedoch möglicherweise auf dem richtigen Computer erfolgreich ausgeführt wird.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird beschrieben, wie Sie eine Verbindung mit einem Remote Computer herstellen, um [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) -Daten abzurufen. Der in " *straudomain* " angegebene Domänen Name wird in "Erstelle" *verwendet.*


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



Der folgende PowerShell-Code Ausschnitt greift auf einen Remote Server zu und listet die verfügbaren WMI-Klassen auf.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch<br/>                                                          |
| IID<br/>                      | IID \_ iswbemlocator<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> </dl>

 

