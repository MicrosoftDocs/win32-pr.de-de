---
title: Registrierungs Werte der EAP-Peer Methode
description: Erfahren Sie mehr über die spezifischen Registrierungs Werte, die für EAP-Peer Methoden erforderlich sind. Hier finden Sie eine Liste der Registrierungs Werte und weitere verfügbare Ressourcen.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316491"
---
# <a name="eap-peer-method-registry-values"></a>Registrierungs Werte der EAP-Peer Methode

Bestimmte Registrierungs Werte sind für EAP-Peer Methoden erforderlich.

## <a name="eap-peer-method-dll-paths"></a>DLL-Pfade der EAP-Peer Methode

Der folgende Pfad gibt den Registrierungs Speicherort für reguläre DLLs der EAP-Peer Methode an.

**HKLM \\ System \\ CCS \\ \\ -Dienste EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ * &lt; eaptypeid&gt;***

Beispielsweise wird ein Registrierungs Pfad für die EAP-Methoden Installation angegeben, der eine **autoriid** von "311" (die besagt, dass "Microsoft" der Autor ist) und die **eaptypeid** "40" erhalten.

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 40**

Der folgende Pfad gibt den Registrierungs Speicherort für erweiterte EAP-Methoden-DLLs an.

> [!Note]  
> Erweiterte EAP-Methoden-DLLs werden in Windows Vista mit Service Pack 1 (SP1) oder höher unterstützt.

 

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ * &lt; eaptypeid&gt;***

Beispielsweise wird ein Registrierungs Pfad der EAP-Methoden Installation mit der **Autorisierung** "311" (die besagt, dass "Microsoft" der Autor ist), der **VendorID** "311" und der **eaptypeid** "40" wie folgt angezeigt.

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Weitere Informationen zur Zuordnung von EAP-Methoden Typen finden Sie im Abschnitt 6,2 von [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Registrierungs Werte

Die folgenden Registrierungs Werte für die EAPHost-Peer Methode sind erforderlich.

-   [Peerdllpath](#peerdllpath)
-   [Peer FriendlyName](#peerfriendlyname)
-   [Peer invokepassworddialog](#peerinvokepassworddialog)
-   [Peer invokeusernamedialog](#peerinvokeusernamedialog)

Die folgenden Registrierungs Werte für die AP-Peer Methode werden empfohlen.

-   [Eigenschaften](#properties)

Die folgenden Registrierungs Werte für die AP-Peer Methode sind optional.

-   [Peerconfiguipath](#peerconfiguipath)
-   [Peeridentitypath](#peeridentitypath)
-   [Peerinteractiveuipath](#peerinteractiveuipath)
-   [Peerrequirements configui](#peerrequireconfigui)

### <a name="peerconfiguipath"></a>Peerconfiguipath



| Konstanter Wert | Peerconfiguipath                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ Expand \_ SZ                                                                                                                                        |
| BESCHREIBUNG    | Der Pfad zur dll, die die Implementierung des Dialog Felds für die Benutzerkonfiguration enthält. Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll. |



 

### <a name="peerdllpath"></a>Peerdllpath



| Konstanter Wert | Peerdllpath                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| type           | REG \_ Expand \_ SZ                                                                                 |
| BESCHREIBUNG    | Der Pfad zur EAP-Methoden-dll. Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll. |



 

### <a name="peerfriendlyname"></a>Peer FriendlyName



| Konstanter Wert | Peer FriendlyName                                                     |
|----------------|----------------------------------------------------------------------|
| type           | REG- \_ SZ                                                              |
| BESCHREIBUNG    | Eine Zeichenfolge, die den anzeigen Amen für die EAP-Methode enthält. |



 

### <a name="peeridentitypath"></a>Peeridentitypath



| Konstanter Wert | Peeridentitypath                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ Expand \_ SZ                                                                                                                                      |
| BESCHREIBUNG    | Der Pfad zur dll, die die Implementierung der Benutzer Identitäts Funktionen enthält. Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll. |



 

### <a name="peerinteractiveuipath"></a>Peerinteractiveuipath



| Konstanter Wert | Peerinteractiveuipath                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ Expand \_ SZ                                                                                                                                                                                                            |
| BESCHREIBUNG    | Der Pfad zur dll, die die Implementierung der interaktiven Benutzeroberfläche enthält, die zum Abrufen von Benutzerinformationen während der Ausführung der EAP-Methode verwendet wird. Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll. |



 

### <a name="peerinvokepassworddialog"></a>Peer invokepassworddialog



| Konstanter Wert | Peer invokepassworddialog                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                                                                                                       |
| BESCHREIBUNG    | 1: um Anmelde Informationen mithilfe des generischen EAPHost-Kennworts und der Domäne zu erhalten. 0-so verwenden Sie ein benutzerdefiniertes Dialogfeld. Wenn das generische Dialogfeld verwendet wird, werden die Anmelde Informationen von der [**eappeersetanmelde**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) -Methode festgelegt. |



 

### <a name="peerinvokeusernamedialog"></a>Peer invokeusernamedialog



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Konstanter Wert</th>
<th>Peer invokeusernamedialog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>REG_DWORD</td>
</tr>
<tr class="even">
<td>BESCHREIBUNG</td>
<td><ul>
<li>1: zum erhalten von Anmelde Informationen im Dialogfeld "generischer EAPHost-Benutzername".</li>
<li>0-so verwenden Sie ein benutzerdefiniertes Dialogfeld.</li>
</ul>
Wenn das generische Dialogfeld verwendet wird, werden die Anmelde Informationen von der [<strong>eappeersetanmelde</strong>Informationen] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials)-Methode festgelegt.</td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a>Peerrequirements configui



| Konstanter Wert | Peerrequirements configui                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                 |
| BESCHREIBUNG    | 0, wenn für diese Methode ein Dialogfeld für die Konfigurations Benutzeroberfläche implementiert ist. 1, wenn dies nicht der Fall ist. |



 

### <a name="properties"></a>Eigenschaften



| Konstanter Wert | Eigenschaften                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                  |
| BESCHREIBUNG    | Bits in DWORD sind so festgelegt, dass die Unterstützung für die Eigenschaft angegeben wird. Eine Liste der unterstützten Werte finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsschlüssel für die EAP-Authenticator-Methode](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[Registrierungs Konfiguration für erweiterte EAP-Typen](registry-keys-for-eap-methods.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 