---
title: Registrierungswerte der EAP-Peermethode
description: Erfahren Sie mehr über die spezifischen Registrierungswerte, die für EAP-Peermethoden erforderlich sind. Sehen Sie sich eine Liste der Registrierungswerte an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee42360689a74b3cd11628e6114e80532000b95f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476636"
---
# <a name="eap-peer-method-registry-values"></a>Registrierungswerte der EAP-Peermethode

Für EAP-Peermethoden sind bestimmte Registrierungswerte erforderlich.

## <a name="eap-peer-method-dll-paths"></a>DLL-Pfade der EAP-Peermethode

Der folgende Pfad gibt den Registrierungsspeicherort für reguläre EAP-Peermethode-DLLs an.

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ * &lt; EapTypeId&gt;***

Beispielsweise wird ein Registrierungspfad für die Installation der EAP-Methode mit der **AuthorId** "311" (der angibt, dass "Microsoft" der Autor ist) und die **EapTypeId** "40" wie folgt angezeigt.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 40**

Der folgende Pfad gibt den Registrierungsspeicherort für erweiterte EAP-Methoden-DLLs an.

> [!Note]  
> Erweiterte EAP-Methoden-DLLs werden in Windows Vista mit Service Pack 1 (SP1) oder höher unterstützt.

 

**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ Methods \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorId &gt;* \\ * &lt; EapTypeId&gt;***

Beispielsweise wird ein Registrierungspfad für die Installation der EAP-Methode mit einer **AuthorId** von "311" (der angibt, dass "Microsoft" der Autor ist), eine **VendorId** von "311" und eine **EapTypeId** von "40" wie folgt angezeigt.

**HKLM \\ System \\ CCS Services \\ \\ Eaphost \\ Methods \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Weitere Informationen zur Zuordnung von EAP-Methodentypen finden Sie in Abschnitt 6.2 von [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Registrierungswerte

Die folgenden Registrierungswerte für die EAPHost-Peermethode sind erforderlich.

-   [PeerDllPath](#peerdllpath)
-   [PeerFriendlyName](#peerfriendlyname)
-   [PeerInvokePasswordDialog](#peerinvokepassworddialog)
-   [PeerInvokeUsernameDialog](#peerinvokeusernamedialog)

Die folgenden Registrierungswerte der AP-Peermethode werden empfohlen.

-   [Eigenschaften](#properties)

Die folgenden Registrierungswerte der AP-Peermethode sind optional.

-   [PeerConfigUIPath](#peerconfiguipath)
-   [PeerIdentityPath](#peeridentitypath)
-   [PeerInteractiveUIPath](#peerinteractiveuipath)
-   [PeerRequireConfigUI](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>PeerConfigUIPath



| Konstanter Wert | PeerConfigUIPath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ EXPAND \_ SZ                                                                                                                                        |
| BESCHREIBUNG    | Der Pfad zur DLL, die die Implementierung des Dialogfelds für die Benutzerkonfiguration enthält. Beispiel: %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerdllpath"></a>PeerDllPath



| Konstanter Wert | PeerDllPath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| type           | REG \_ EXPAND \_ SZ                                                                                 |
| BESCHREIBUNG    | Der Pfad zur EAP-Methoden-DLL. Beispiel: %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerfriendlyname"></a>PeerFriendlyName



| Konstanter Wert | PeerFriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| type           | REG \_ SZ                                                              |
| BESCHREIBUNG    | Eine Zeichenfolge, die den Anzeigenamen für die EAP-Methode enthält. |



 

### <a name="peeridentitypath"></a>PeerIdentityPath



| Konstanter Wert | PeerIdentityPath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ EXPAND \_ SZ                                                                                                                                      |
| BESCHREIBUNG    | Der Pfad zur DLL, die die Implementierung der Benutzeridentitätsfunktionen enthält. Beispiel: %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerinteractiveuipath"></a>PeerInteractiveUIPath



| Konstanter Wert | PeerInteractiveUIPath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ EXPAND \_ SZ                                                                                                                                                                                                            |
| BESCHREIBUNG    | Der Pfad zur DLL, die die Implementierung der interaktiven Benutzeroberfläche enthält, die zum Abrufen von Benutzerinformationen während der Ausführung der EAP-Methode verwendet wird. Beispiel: %SystemRoot% \\ system32 \\ &lt; name of DLL \_ \_ &gt;.dll. |



 

### <a name="peerinvokepassworddialog"></a>PeerInvokePasswordDialog



| Konstanter Wert | PeerInvokePasswordDialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                                                                                                       |
| BESCHREIBUNG    | 1: Zum Erhalten von Anmeldeinformationen mithilfe des generischen Dialogfelds EAPHost-Kennwort und Domäne. 0 : , um ein benutzerdefiniertes Dialogfeld zu verwenden. Wenn das generische Dialogfeld verwendet wird, werden Anmeldeinformationen von der [**EapPeerSetCredentials-Methode**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) festgelegt. |



 

### <a name="peerinvokeusernamedialog"></a>PeerInvokeUsernameDialog




| Konstanter Wert | PeerInvokeUsernameDialog | 
|----------------|--------------------------|
| type | REG_DWORD | 
| BESCHREIBUNG | <ul><li>1: Zum Erhalten von Anmeldeinformationen mithilfe des generischen Dialogfelds EAPHost-Benutzername.</li><li>0: , um ein benutzerdefiniertes Dialogfeld zu verwenden.</li></ul>Wenn das generische Dialogfeld verwendet wird, werden Anmeldeinformationen von der [<strong>EapPeerSetCredentials-Methode</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) festgelegt. | 




 

### <a name="peerrequireconfigui"></a>PeerRequireConfigUI



| Konstanter Wert | PeerRequireConfigUI                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                 |
| BESCHREIBUNG    | 0, wenn ein Konfigurationsdialogfeld für die Benutzeroberfläche für diese Methode implementiert ist; 1, wenn dies nicht der Dere ist. |



 

### <a name="properties"></a>Eigenschaften



| Konstanter Wert | Eigenschaften                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                  |
| BESCHREIBUNG    | Bits im DWORD werden festgelegt, um die Unterstützung für die -Eigenschaft anzugeben. Eine Liste der unterstützten Werte finden Sie unter [**EAP-Methodeneigenschaften.**](eap-method-properties.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsschlüssel Authenticator EAP-Methode](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Registrierungskonfiguration für erweiterte EAP-Typen](registry-keys-for-eap-methods.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 
