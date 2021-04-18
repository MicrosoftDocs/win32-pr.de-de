---
title: Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt
description: Sie können die Methoden Session. identifioder iwsmansession. identifiverwenden, um zu bestimmen, ob der Remote Computer über einen Dienst verfügt, der das WS-Management Protokoll unterstützt.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338994"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt

Sie können die Methoden [**Session. identifioder**](session-identify.md) [**iwsmansession. identifiverwenden**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) , um zu bestimmen, ob der Remote Computer über einen Dienst verfügt, der das WS-Management Protokoll unterstützt.

Wenn ein WS-Management Protokolldienst auf dem Remote Computer konfiguriert ist und auf Anforderungen lauscht, kann der Dienst eine Erkennungs Anforderung mit dem folgenden XML-Code in der Kopfzeile erkennen.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Der WS-Management Protokolldienst, der die Anforderung empfängt, gibt die Informationen, die in der folgenden Liste enthalten sind, im Nachrichtentext zurück:

-   Die WS-Management Protokollversion. Beispiel: „https://schemas.dmtf.org/wbem/wsman/1/wsman“.
-   Der Produkthersteller, z. b. "Microsoft Corporation".
-   Die Produktversion. Wenn die Anforderung mit **wsmanflagusenoauthentication** im *Flags* -Parameter gesendet wird, werden keine Produkt Versionsinformationen zurückgegeben. Wenn die Anforderung entweder mit der Standard Authentifizierung oder mit einem anderen angegebenen Authentifizierungsmodus gesendet wird, können die Produkt Versionsinformationen zurückgegeben werden.

Die Anforderung, zu ermitteln, ob der Remote Computer über einen konfigurierten und lauschenden WS-Management Protokolldienst am Anfang eines Skripts mit anderen Vorgängen ausgeführt werden kann. Dadurch wird überprüft, ob der Bereitstellungs Zielcomputer auf Weitere WS-Management Protokoll Anforderungen reagieren kann. Die Überprüfung kann auch in einem separaten Skript durchgeführt werden.

**So erkennen Sie einen WS-Management Protokolldienst**

1.  Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Legen Sie fest, ob die Anforderung authentifiziert oder nicht authentifiziert gesendet werden soll, und legen Sie den *Flags* -Parameter entsprechend im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen fest.

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  " [**Session. Identifi"**](session-identify.md)aufzurufen.

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel sendet eine nicht authentifizierte Identifizierungs Anforderung an den Remote Computer mit dem Namen "remote1" in derselben Domäne.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



Die folgende Antwort zeigt den XML-Code, der vom Remote Computer zurückgegeben wurde. Die WS-Management-Protokollversion (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") und der Betriebssystemhersteller ("Microsoft Corporation") werden in der zurückgegebenen XML-Datei angegeben. Da die Nachricht nicht authentifiziert gesendet wird, wird die Produktversion nicht vom Windows-Remoteverwaltung-Dienst zurückgegeben.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



Im folgenden VBScript-Codebeispiel wird eine authentifizierte Identifizierungs Anforderung an den Remote Computer gesendet.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Da die Anforderung mit der Authentifizierung gesendet wurde, werden die Versionsinformationen zurückgegeben.


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

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 




