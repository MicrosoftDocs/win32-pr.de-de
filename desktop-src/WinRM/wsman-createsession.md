---
title: WSMAN. kreatesession-Methode (WSManDisp. h)
description: Erstellt ein Sitzungs Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreatesession"
- Die Methode "kreatesession" Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreatesession"
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
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518143"
---
# <a name="wsmancreatesession-method"></a>WSMAN. kreatesession-Methode

Erstellt ein [**Sitzungs**](session.md) Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.

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

Das Protokoll und der Dienst, mit denen eine Verbindung hergestellt werden soll, einschließlich IPv4 oder IPv6. Das Format der Verbindungsinformationen lautet wie folgt: <*Transport* >< *Adress* >< *Suffix*>. Beispiele finden Sie unter Hinweise. Wenn keine Verbindungsinformationen bereitgestellt werden, wird der lokale Computer verwendet.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Die Sitzungsflags, die die Authentifizierungsmethode angeben, z. b. [*Aushandlung der Authentifizierung*](windows-remote-management-glossary.md) oder [*Digestauthentifizierung*](windows-remote-management-glossary.md)zum Herstellen einer Verbindung mit einem Remote Computer. Diese Flags geben auch andere Sitzungs Verbindungsinformationen an, z. b. Codierung oder Verschlüsselung. Dieser Parameter muss mindestens eines der Flags in **\_ \_ wsmansessionflags** für eine Remote Verbindung enthalten. Weitere Informationen finden Sie unter [Sitzungs Konstanten](session-constants.md). Für eine Verbindung mit WinRM auf dem lokalen Computer sind keine Flag-Einstellungen erforderlich. Der Standardwert ist " **wsmanflagusenegotiate**".

Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md) und *ConnectionOptions* -Parameter.

</dd> <dt>

*ConnectionOptions* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein [**ConnectionOptions**](connectionoptions.md) -Objekt, das einen Benutzernamen und ein Kennwort enthält. Der Standardwert ist **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Sitzungs**](session.md) Objekt, das dann zum Ausführen von lokalen oder Remote-WinRM-Vorgängen verwendet werden kann.

## <a name="remarks"></a>Bemerkungen

Die Methode " **kreatesession** " initialisiert das [**Sitzungs**](session.md) Objekt, indem Parameter, wie z. b. Flags, Anmelde Informationen und eine Verbindungs Zeichenfolge für den *Verbindungs* Parameter, gesammelt werden. " **Anatesession** " stellt keine Verbindung mit dem lokalen Computer oder dem Remote Computer her. Wenn die Verbindung nicht hergestellt werden kann, tritt beim ersten **Sitzungs** Vorgang (z. b. [**Get**](session-get.md) oder [**Enumerate**](session-enumerate.md)) nach dem Aufrufen von " **anatesession**" ein Fehler auf. Dieses Verhalten unterscheidet sich von einer [*WMI*](windows-remote-management-glossary.md) -Verbindung mit einem [*Namespace*](windows-remote-management-glossary.md) auf einem Remote Computer. Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).

Das folgende VBScript-Codebeispiel wird verwendet, um diese Methode aufzurufen.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



In den folgenden Beispielen werden die unterschiedlichen Formate zum Angeben von Verbindungsinformationen im *Verbindungs* Parameter veranschaulicht (beim Erstellen einer HTTPS-Sitzung muss das Feld <*Adresse*> mit dem Namen des Server Computer Zertifikats identisch sein, andernfalls tritt ein Fehler auf):

-   "https://service"

    Verwendet HTTPS zum Herstellen der Verbindung mit dem Standardweb Dienst-Speicherort.

-   "https://service.corp.com/websvcs/wsman"

    Verwendet HTTPS zum Herstellen der Verbindung mit dem spezifischen Webdienst Speicherort.

-   "https:// \[ E3D7:0000:0000:0000:51F 4:9bc8: c0a8:6420 \] "

    Verwendet HTTPS und IPv6 mit dem Standardport.

-   "https:// \[ E3D7:0000:0000:0000:51F 4:9bc8: c0a8:6420 \] : 9999/WSMAN"

    Verwendet HTTPS und IPv6 mit dem angegebenen Port.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird eine Sitzung auf dem lokalen Computer erstellt.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



Im folgenden VBScript-Codebeispiel wird eine Sitzung auf einem Remote Computer erstellt, der durch eine IP-Adresse identifiziert wird. Das Skript stellt einen Benutzernamen und ein Kennwort für ein Konto bereit. Die Flags **wsmanflagkredusernamepassword** und **wsmanflagusebasic** werden kombiniert, um anzugeben, dass es sich bei dem Konto um ein lokales Konto auf dem Remote Computer handelt. Wenn die Erstellung der Sitzung fehlschlägt, wird das Skript beendet. Das Skript verwendet die Methoden, die die Konstante zurückgeben, z. b. [**WSMAN. sessionflagusebasic**](wsman-sessionflagusebasic.md).

Beachten Sie beim Ausführen dieses Skripts, dass Sie die Standard Konfigurationseinstellungen für Client und Server so konfigurieren müssen, dass unverschlüsselter Datenverkehr und die Standard Authentifizierung zulässig sind ("'" auf **true** und "Basic" auf " **true****" festgelegt** ist). Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



Im folgenden VBScript-Codebeispiel handelt es sich bei dem Konto um ein Domänen Konto, und Aushandlungs Authentifizierung wird verwendet. Bei der Aushandlung der Authentifizierung müssen Sie den Benutzernamen als `computername\username` oder angeben `ipaddress\username` .


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> <dt>

[Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md)
</dt> <dt>

[Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





