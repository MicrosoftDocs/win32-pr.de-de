---
title: WSMan.CreateSession-Methode (WSManDisp.h)
description: Erstellt ein Session-Objekt, das dann für nachfolgende Netzwerkvorgänge verwendet werden kann.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- CreateSession-Methode Windows Remoteverwaltung
- CreateSession-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung, CreateSession-Methode
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330f8ea6456001c7e3b81dfbfeb07a125d30a5069596ef7d4f3e6ad561994ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742603"
---
# <a name="wsmancreatesession-method"></a>WSMan.CreateSession-Methode

Erstellt ein [**Session-Objekt,**](session.md) das dann für nachfolgende Netzwerkvorgänge verwendet werden kann.

## <a name="syntax"></a>Syntax


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ in, optional\]
</dt> <dd>

Das Protokoll und der Dienst, mit dem eine Verbindung hergestellt werden soll, einschließlich IPv4 oder IPv6. Das Format der Verbindungsinformationen lautet wie folgt: <*transport* >< *address* >< *suffix>.* Beispiele finden Sie unter Hinweise. Wenn keine Verbindungsinformationen angegeben werden, wird der lokale Computer verwendet.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Die Sitzungsflags, die die [](windows-remote-management-glossary.md) Authentifizierungsmethode angeben, z. B. Negotiate-Authentifizierung oder [*Digestauthentifizierung,*](windows-remote-management-glossary.md)zum Herstellen einer Verbindung mit einem Remotecomputer. Diese Flags geben auch andere Sitzungsverbindungsinformationen an, z. B. Codierung oder Verschlüsselung. Dieser Parameter muss mindestens eines der Flags in **\_ \_ WSManSessionFlags** für eine Remoteverbindung enthalten. Weitere Informationen finden Sie unter [Sitzungskonst konstanten](session-constants.md). Für eine Verbindung mit WinRM auf dem lokalen Computer sind keine Flageinstellungen erforderlich. Der Standardwert ist **WSManFlagUseNegotiate.**

Weitere Informationen finden Sie unter [Authentifizierung für Remoteverbindungen](authentication-for-remote-connections.md) und *connectionOptions-Parameter.*

</dd> <dt>

*connectionOptions* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein [**ConnectionOptions-Objekt,**](connectionoptions.md) das einen Benutzernamen und ein Kennwort enthält. Der Standardwert ist **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [](session.md) Session-Objekt, das dann verwendet werden kann, um lokale oder Remote-WinRM-Vorgänge durchzuführen.

## <a name="remarks"></a>Hinweise

Die **CreateSession-Methode** initialisiert das [**Session-Objekt**](session.md) durch Sammeln von Parametern wie Flags, Anmeldeinformationen und einer Verbindungszeichenfolge für den *Verbindungsparameter.* **CreateSession** stellt tatsächlich keine Verbindung mit dem lokalen Computer oder Remotecomputer herstellen. Wenn die Verbindung nicht hergestellt werden kann,  tritt nach dem [](session-get.md) Aufruf von CreateSession ein Fehler beim ersten Sitzungsvorgang auf, z. B. beim Get- oder [**Enumerate-Vorgang.**](session-enumerate.md)  Dieses Verhalten unterscheidet sich von [*einer WMI-Verbindung*](windows-remote-management-glossary.md) mit einem [*Namespace*](windows-remote-management-glossary.md) auf einem Remotecomputer. Weitere Informationen finden Sie unter [Windows Remoteverwaltung und WMI.](windows-remote-management-and-wmi.md)

Das folgende VBScript-Codebeispiel wird zum Aufrufen dieser Methode verwendet.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



Die folgenden Beispiele zeigen die verschiedenen Formate  zum Angeben von Verbindungsinformationen im Verbindungsparameter (beim Erstellen einer HTTPS-Sitzung muss das Feld <*Address*> mit dem Zertifikatnamen des Servercomputers übereinstimmen, andernfalls tritt ein Fehler auf:

-   "https://service"

    Verwendet HTTPS, um eine Verbindung mit dem Standardspeicherort des Webdiensts herzustellen.

-   "https://service.corp.com/websvcs/wsman"

    Verwendet HTTPS, um eine Verbindung mit dem spezifischen Webdienststandort herzustellen.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420 \] "

    Verwendet HTTPS und IPv6 mit dem Standardport.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420 \] :9999/wsman"

    Verwendet HTTPS und IPv6 mit dem angegebenen Port.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird eine Sitzung auf dem lokalen Computer erstellt.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



Im folgenden VBScript-Codebeispiel wird eine Sitzung auf einem Remotecomputer erstellt, der durch eine IP-Adresse identifiziert wird. Das Skript gibt einen Benutzernamen und ein Kennwort für ein Konto an. Die Flags **WSManFlagCredUserNamePassword** und **WSManFlagUseBasic** werden kombiniert, um anzugeben, dass das Konto ein lokales Konto auf dem Remotecomputer ist. Wenn die Erstellung der Sitzung fehlschlägt, wird das Skript beendet. Das Skript verwendet die Methoden, die die Konstante zurückgeben, [**z.B. WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).

Beachten Sie zum Ausführen dieses Skripts, dass Sie die Standardkonfigurationseinstellungen für Client und Server so konfigurieren müssen, dass unverschlüsselter Datenverkehr und Standardauthentifizierung zulässig sind (**AllowUnencrypted** auf **True** und Basic auf **True** festgelegt). Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



Im folgenden VBScript-Codebeispiel ist das Konto ein Domänenkonto, und die Negotiate-Authentifizierung wird verwendet. Bei der Negotiate-Authentifizierung müssen Sie den Benutzernamen als oder `computername\username` `ipaddress\username` angeben.


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> <dt>

[Authentifizierung für Remoteverbindungen](authentication-for-remote-connections.md)
</dt> <dt>

[Installation und Konfiguration für Windows Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





