---
title: Erkennen, ob ein Remotecomputer das WS-Management unterstützt
description: Sie können die Methoden Session.Identify oder IWSManSession.Identify verwenden, um zu bestimmen, ob der Remotecomputer über einen Dienst verfügt, der das WS-Management unterstützt.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a7ebeb25f7f3af69a03c55499dd53a890e540c1a1ed677e7d48e5b11b82b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643230"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Erkennen, ob ein Remotecomputer das WS-Management unterstützt

Sie können die [**Methoden Session.Identify**](session-identify.md) oder [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) verwenden, um zu bestimmen, ob der Remotecomputer über einen Dienst verfügt, der das WS-Management unterstützt.

Wenn ein WS-Management-Protokolldienst auf dem Remotecomputer konfiguriert ist und auf Anforderungen lausiert, kann der Dienst eine Identify-Anforderung durch den folgenden XML-Code im Header erkennen.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Der WS-Management Protokolldienst, der die Anforderung empfängt, gibt die In der folgenden Liste enthaltenen Informationen im Nachrichtentext zurück:

-   Die WS-Management Protokollversion. Beispiel: „https://schemas.dmtf.org/wbem/wsman/1/wsman“.
-   Der Produkthersteller, z. B. "Microsoft Corporation".
-   Die Produktversion. Wenn die Anforderung mit **WSManFlagUseNoAuthentication** im *flags-Parameter* gesendet wird, werden keine Produktversionsinformationen zurückgegeben. Wenn die Anforderung entweder mit der standardbasierten Authentifizierung oder mit einem anderen angegebenen Authentifizierungsmodus gesendet wird, können die Produktversionsinformationen zurückgegeben werden.

Die Anforderung zur Erkennung, ob der Remotecomputer über einen konfigurierten und lauschenden Protokolldienst verfügtWS-Management kann am Anfang eines Skripts mit anderen Vorgängen ausgeführt werden. Dadurch wird überprüft, ob die Zielcomputer auf weitere Protokollanforderungen WS-Management können. Die Überprüfung kann auch in einem separaten Skript erfolgen.

**So erkennen Sie WS-Management Protokolldienst**

1.  Erstellen Sie ein [**WSMan-Objekt.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Bestimmen Sie, ob die Anforderung authentifiziert oder nicht authentifiziert gesendet werden soll, und legen Sie den *flags-Parameter* im Aufruf von [**WSMan.CreateSession entsprechend fest.**](wsman-createsession.md)

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Rufen Sie [**Session.Identify auf.**](session-identify.md)

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird eine nicht authentifizierte Identify-Anforderung an den Remotecomputer mit dem Namen "Remote1" in derselben Domäne sendet.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



Die folgende Antwort zeigt den vom Remotecomputer zurückgegebenen XML-Code. Die WS-Management Protokollversion (" ") und der Betriebssystemanbieter https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ("Microsoft Corporation") werden im zurückgegebenen XML-Code angegeben. Da die Nachricht nicht authentifiziert gesendet wird, wird die Produktversion nicht vom Remoteverwaltungsdienst Windows zurückgegeben.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



Im folgenden VBScript-Codebeispiel wird eine authentifizierte Identify-Anforderung an den Remotecomputer sendet.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Da die Anforderung mit Authentifizierung gesendet wurde, werden die Versionsinformationen zurückgegeben.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows Remoteverwaltungsreferenz](windows-remote-management-reference.md)
</dt> </dl>

 

 




