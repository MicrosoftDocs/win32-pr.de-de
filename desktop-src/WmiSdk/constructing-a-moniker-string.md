---
description: Das Format der Monikerzeichenfolge ähnelt einem standardmäßigen WMI-Objekt Pfad. Weitere Informationen finden Sie unter WMI-Objekt Pfad Anforderungen.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Erstellen einer Monikerzeichenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344938"
---
# <a name="constructing-a-moniker-string"></a>Erstellen einer Monikerzeichenfolge

Das Format der Monikerzeichenfolge ähnelt einem standardmäßigen WMI-Objekt Pfad. Weitere Informationen finden Sie unter [WMI-Objekt Pfad Anforderungen](wmi-object-path-requirements.md).

Ein Moniker besteht aus den folgenden Teilen:

-   Das Präfix winmgmts: (obligatorisch). Das Präfix weist den Windows Script Host (WSH) an, dass der folgende Code die [Skript-API-Objekte](scripting-api-objects.md)verwendet.
-   Eine Sicherheits Einstellungs Komponente (optional)
-   Eine WMI-Objekt Pfadkomponente (optional)

Ein Kennwort kann nicht in einer WMI-Monikerzeichenfolge angegeben werden. Wenn Sie beim Herstellen einer Verbindung mit WMI das Kennwort ("*stranpassword* "-Parameter) oder den Authentifizierungstyp ("*chanauthority* ") ändern müssen, dann wenden Sie sich an "WS. [**ConnectServer**](swbemlocator-connectserver.md)". Beachten Sie, dass Sie nur das Kennwort und die Autorität in Verbindungen mit Remote Computern angeben können. Der Versuch, diese in einem Skript festzulegen, das auf dem lokalen Computer ausgeführt wird, führt zu einem Fehler. Weitere Informationen dazu, wann die Sicherheitseinstellungen und Objekt Pfad Komponenten verwendet werden, finden Sie unter [WMI-Sicherheitseinstellungen](/previous-versions/tn-archive/ee156574(v=technet.10)).

Der folgende Moniker gibt das [**Swap Services**](swbemservices.md) -Objekt an, das den Standardwert für den Namespace Stamm darstellt, bei dem der Identitätswechsel \\ aktiviert ist und die wbemprivilegedebug-Berechtigung (SeDebugPrivilege) aktiviert und die wbemprivilegesection-Berechtigung (SeSecurityPrivilege) deaktiviert ist.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Bei allen Zeichen folgen literalen wird Groß-/Kleinschreibung nicht beachtet
>
> Mit dem Präfix "!" für eine Berechtigung wird angegeben, dass die Berechtigung deaktiviert werden soll. das Weglassen dieses Präfixes impliziert, dass die Berechtigung aktiviert werden muss.
>
> Das Präfix "!" wird für den Computernamen oder den Namespace verwendet, wenn die Sicherheitseinstellungen vor dem Computernamen oder Namespace in Klammern angegeben werden.

 

Die folgenden Standard Zuweisungen sind zulässig, wenn der Objekt Pfad angegeben wird:

-   Der Computername des Computers kann im Objekt Pfad weggelassen werden. in diesem Fall wird der Name des lokalen Computers angenommen.
-   Der Namespace kann im Objekt Pfad weggelassen werden. in diesem Fall wird der Standard Namespace angenommen.

    Dies wird durch den Wert des Registrierungsschlüssels **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard Namespace** festgelegt. der Standardwert ist "root \\ CIMv2".

-   Es kann auch eine Klasse oder eine Instanz angegeben werden. in diesem Fall handelt es sich bei dem zurückgegebenen Objekt um ein WMI-Objekt und nicht um ein Dienst Objekt.

> [!Note]  
> Wenn eine Klasse oder eine Instanz angegeben ist, können Sie den Namespace nicht weglassen, wenn Sie den Computernamen angeben.

 

Einen Verweis auf die für die WMI-Monikerzeichenfolge verwendeten Berechtigungs Konstanten finden Sie unter [Berechtigungs Konstanten](privilege-constants.md)und in den Deskriptoren "Skript-Kurzname".

## <a name="valid-moniker-strings"></a>Gültige Monikerzeichenfolgen

In den folgenden Beispielen werden gültige Monikerzeichenfolgen veranschaulicht.

Der folgende Moniker identifiziert den Standard Namespace auf dem lokalen Computer. Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.


```VB
WinMgmts:
```



Der folgende Moniker identifiziert den Standard Namespace auf dem Computer "MyServer". Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.


```VB
"WinMgmts://myServer"
```



Der folgende Moniker identifiziert den root \\ CIMV2-Namespace auf dem MyServer-Computer. Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.


```VB
"WinMgmts://myServer/root/cimv2"
```



Der folgende Moniker identifiziert den root \\ CIMV2-Namespace auf dem lokalen Server. Ein [**-**](swbemservices.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:root/cimv2"
```



Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im root \\ CIMV2-Namespace auf dem MyServer-Server. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im root \\ CIMV2-Namespace auf dem lokalen Server. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



Der folgende Moniker identifiziert die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse im Standard Namespace auf dem lokalen Server. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im Standard-Skript Namespace auf dem lokalen Server entspricht. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben. Der Standard Namespace für die Skripterstellung wird durch die standardmäßige Namespace-Konfigurationseinstellung festgelegt, wie im WMI-Steuerelement angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im root \\ CIMV2-Namespace auf dem MyServer-Server entspricht. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im root \\ CIMV2-Namespace auf dem lokalen Server entspricht. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



Der folgende Moniker identifiziert die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , die dem Laufwerk C: im Standard Namespace auf dem lokalen Server entspricht. Ein [**-**](swbemobject.md) Objekt wird zurückgegeben.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



Der folgende Moniker legt die Identitätswechsel Ebene fest, um die Identität anzunehmen, und legt die SE- \_ Debugberechtigung fest.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



Der folgende Moniker legt die Identitätswechsel Ebene fest, um die Identität anzunehmen, und legt die SE- \_ Debugberechtigung fest. Außerdem wird das Recht zum Herunterfahren der Berechtigung aufgehoben \_ .


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



Der folgende Moniker ruft in englischer Sprache lokalisierte Beschreibungen für die Klasse **MyClass** aus dem \\ WMI-Stamm Namespace ab.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



Der folgende Moniker fordert die Kerberos-Authentifizierung mithilfe des Prinzipal Servers "mydomain" an \\ .


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



Der folgende Moniker fordert die NTLM-Authentifizierung mithilfe der mydomain-Domäne an.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sicherheits-und Gebiets Schema Parameter in einem Moniker kombiniert werden.


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Obwohl Moniker einen direkteren Zugriff auf Objekte bereitstellen, kann die wiederholte Verwendung von Monikern unter bestimmten Umständen weniger effizient sein als der äquivalente Code, der explizit eine Verbindung mit WMI herstellt. Wenn die Anwendungsleistung zu beachten ist, sollten Sie die Verwendung der alternativen Mechanismen in Erwägung ziehen.
>
> Es ist nicht möglich, die **GetObject** -Funktion von VBScript zum Aktualisieren oder Festlegen von Daten zu verwenden, wenn Skripts ausgeführt werden, die in einer HTML-Seite eingebettet sind, da Microsoft Internet Explorer die Verwendung dieses aufrupts aus Sicherheitsgründen verweigert.

 

 

 
