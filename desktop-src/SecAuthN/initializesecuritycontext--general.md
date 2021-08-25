---
description: Initiiert den clientseitigen ausgehenden [*Sicherheitskontext von*](../secgloss/s-gly.md) einem Anmeldeinformationshand handle.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: InitializeSecurityContext (General)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: e0a4b1b9ff38faa840667f513aee25d61c23180d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627366"
---
# <a name="initializesecuritycontext-general-function"></a>InitializeSecurityContext(General)-Funktion

Die **InitializeSecurityContext (General)-Funktion** initiiert den clientseitigen ausgehenden Sicherheitskontext [*von*](../secgloss/s-gly.md) einem Anmeldeinformationshand handle. Die -Funktion wird verwendet, um einen [*Sicherheitskontext zwischen*](../secgloss/s-gly.md) der Clientanwendung und einem Remote-Peer zu erstellen. **InitializeSecurityContext (Allgemein)** gibt ein Token zurück, das der Client an den Remote-Peer übergeben muss, den der Peer wiederum über den [**AcceptSecurityContext (General)-Aufruf**](acceptsecuritycontext--general.md) an die lokale Sicherheitsimplementierung übermittelt. Das generierte Token sollte von allen Aufrufern als nicht transparent betrachtet werden.

In der Regel wird die **InitializeSecurityContext (General)-Funktion** in einer Schleife aufgerufen, bis ein ausreichender [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wird.

Informationen zur Verwendung dieser Funktion mit einem bestimmten Sicherheitssupportanbieter (Security [*Support Provider,*](../secgloss/s-gly.md) SSP) finden Sie in den folgenden Themen.



| Thema                                                                                  | Beschreibung                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshand handle mithilfe des CredSSP-Sicherheitspakets (Credential Security Support [*Provider).*](../secgloss/s-gly.md)  
| [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)       | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshand handle mithilfe des [*Digestsicherheitspakets*](../secgloss/s-gly.md).                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshand handle mithilfe des [*Kerberos-Sicherheitspakets*](../secgloss/s-gly.md).                      |
| [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshand handle mithilfe des [*Negotiate-Sicherheitspakets.*](../secgloss/s-gly.md)                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshandl mithilfe des NTLM-Sicherheitspakets. [](../secgloss/s-gly.md)                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext aus einem Anmeldeinformationshandle mithilfe des Schannel-Sicherheitspakets . [](../secgloss/s-gly.md)                      |



 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phCredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmeldeinformationen, die [**von AcquireCredentialsHandle (Allgemein) zurückgegeben werden.**](acquirecredentialshandle--general.md) Dieses Handle wird verwendet, um den [*Sicherheitskontext zu erstellen.*](../secgloss/s-gly.md) Die **InitializeSecurityContext(General)-Funktion** erfordert mindestens OUTBOUND-Anmeldeinformationen.

</dd> <dt>

*phContext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Allgemein)** ist dieser Zeiger **NULL.** Beim zweiten Aufruf ist dieser Parameter ein Zeiger auf das Handle auf den teilweise gebildeten Kontext, der durch den ersten Aufruf im *phNewContext-Parameter* zurückgegeben wird.

Dieser Parameter ist mit dem Microsoft Digest SSP optional und kann auf **NULL festgelegt werden.**

Wenn Sie den Schannel-SSP verwenden, geben Sie beim ersten Aufruf von **InitializeSecurityContext (General)** **NULL an.** Geben Sie bei zukünftigen Aufrufen das Token an, das nach dem ersten Aufruf dieser Funktion im *parameter phNewContext* empfangen wurde.

</dd> <dt>

*pTargetName* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die das Ziel des Kontexts angibt. Die Zeichenfolgeninhalte [*sind sicherheitspaketspezifisch,*](../secgloss/s-gly.md) wie in der folgenden Tabelle beschrieben. Diese Liste ist nicht vollständig. Einem System können zusätzliche System-SSPs und SSPs von Drittanbietern hinzugefügt werden.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Verwendeter SSP</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Digest</strong></dt><dt></dt> </dl></td><td>Auf NULL beendete Zeichenfolge, die den URI der angeforderten Ressource eindeutig identifiziert. Die Zeichenfolge muss aus Zeichen bestehen, die in einem URI zulässig sind, und muss vom US-ASCII-Codesatz darstellbar sein. Die Prozentcodierung kann verwendet werden, um Zeichen außerhalb des US-ASCII-Codesatzes zu darstellen.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos oder Negotiate</strong></dt><dt></dt> </dl></td><td>Dienstprinzipalname (SPN) oder [*der Sicherheitskontext*](../secgloss/s-gly.md) des Zielservers.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Dienstprinzipalname (SPN) oder [*der Sicherheitskontext*](../secgloss/s-gly.md) des Zielservers.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Auf NULL beendete Zeichenfolge, die den Zielserver eindeutig identifiziert. Schannel verwendet diesen Wert, um das Serverzertifikat zu überprüfen. Schannel verwendet diesen Wert auch, um die Sitzung beim Wiederherstellen einer Verbindung im Sitzungscache zu suchen. Die zwischengespeicherte Sitzung wird nur verwendet, wenn alle der folgenden Bedingungen erfüllt sind:<ul><li>Der Zielname ist identisch.</li><li>Der Cacheeintrag ist nicht abgelaufen.</li><li>Der Anwendungsprozess, der die Funktion aufruft, ist identisch.</li><li>Die Anmeldesitzung ist identisch.</li><li>Das Handle für Anmeldeinformationen ist identisch.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC REQ, z. \_ \_ B. ISC \_ REQ \_ DELEGATE. Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Das [*Sicherheitspaket*](../secgloss/s-gly.md) ordnet Ausgabepuffer für Sie zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie sie frei, indem Sie die Funktion [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Verschlüsseln Sie Nachrichten mithilfe der Funktion [<strong>EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen. Dieser Wert ist der Standardwert für die eingeschränkten Kerberos-, Negotiate- und [*NTLM-Delegierungen.*](../secgloss/s-gly.md)<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Der Server kann den Kontext verwenden, um sich bei anderen Servern als Client zu authentifizieren. Das ISC_REQ_MUTUAL_AUTH flag muss festgelegt werden, damit dieses Flag funktioniert. Gültig für Kerberos. Ignorieren Sie dieses Flag für [*die eingeschränkte Delegierung.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Wenn Fehler auftreten, wird die Remote-Partei benachrichtigt.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Verwenden Sie digest für HTTP. Dieses Flag weglassen, um Digest als SASL-Mechanismus zu verwenden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Signieren Sie Nachrichten, und überprüfen Sie Signaturen mithilfe der Funktionen [<strong>EncryptMessage</strong>](encryptmessage--general.md) und [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>Schannel darf den Server nicht automatisch authentifizieren.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Die Richtlinie für gegenseitige Authentifizierung des Diensts wird erfüllt.<br/><blockquote>[!Caution]<br />
Dies bedeutet nicht notwendigerweise, dass die gegenseitige Authentifizierung erfolgt, sondern nur, dass die Authentifizierungsrichtlinie des Diensts erfüllt ist. Rufen Sie die Funktion [<strong>QueryContextAttributes (General)</strong>](querycontextattributes--general.md) auf, um sicherzustellen, dass die gegenseitige Authentifizierung ausgeführt wird.</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Wenn dieses Flag festgelegt ist, wird <strong>ISC_REQ_INTEGRITY</strong> Flag ignoriert.<br/> Dieser Wert wird nur von den eingeschränkten Delegierungen [*Negotiate*](../secgloss/s-gly.md)und Kerberos unterstützt.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Erkennen Sie wiedergegebene Nachrichten, die mithilfe der Funktionen [<strong>EncryptMessage</strong>](encryptmessage--general.md) oder [<strong>MakeSignature</strong>](makesignature.md) codiert wurden.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Unterstützung einer streamorientierten Verbindung.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Ein neuer [*Sitzungsschlüssel*](../secgloss/s-gly.md) muss ausgehandelt werden.<br/> Dieser Wert wird nur von der [*eingeschränkten Kerberos-Delegierung*](../secgloss/s-gly.md)unterstützt.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>Schannel darf nicht versuchen, Anmeldeinformationen für den Client automatisch anzugeben.<br/></td></tr></tbody></table>



 

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

</dd> <dt>

*Reserviert1* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

Dieser Parameter wird nicht mit Digest oder Schannel verwendet. Legen Sie ihn auf 0 (null) fest.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Sofern der Clientkontext nicht vom Server initiiert wurde, muss der Wert dieses Parameters beim ersten Aufruf der Funktion **NULL** sein. Bei nachfolgenden Aufrufen der Funktion oder wenn der Clientkontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der mit genügend Arbeitsspeicher für das vom Remotecomputer zurückgegebene Token zugeordnet ist.

</dd> <dt>

*Reserviert2* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Allgemein)** empfängt dieser Zeiger das neue Kontexthandle. Beim zweiten Aufruf kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

Wenn Sie den Schannel-SSP verwenden, übergeben Sie bei Aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phContext-Parameter,* und geben Sie **NULL** für *phNewContext an.*

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) enthält, die die Ausgabedaten empfängt. Wenn ein Puffer in der Eingabe als SEC \_ READWRITE eingegeben wurde, ist er bei der Ausgabe vorhanden. Das System ordnet auf Anforderung (über ISC REQ ALLOCATE MEMORY) einen Puffer für das Sicherheitstoken zu \_ und gibt die Adresse im \_ \_ Pufferdeskriptor für das Sicherheitstoken ein.

Bei Verwendung des Microsoft Digest SSP empfängt dieser Parameter die Abfrageantwort, die an den Server gesendet werden muss.

Wenn bei Verwendung des Schannel-SSP das ISC \_ REQ \_ ALLOCATE \_ MEMORY-Flag angegeben ist, belegt der Schannel-SSP Speicher für den Puffer und legt die entsprechenden Informationen in [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)ab. Darüber hinaus muss der Aufrufer einen Puffer vom Typ **SECBUFFER \_ ALERT** übergeben. Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, um einen Satz von Bitflags zu empfangen, die die [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ RET, z. B. ISC \_ RET \_ DELEGATE. Eine Liste gültiger Werte finden Sie im *fContextReq-Parameter.*

Suchen Sie erst nach sicherheitsrelevanten Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wurde. Attributflags, die nicht mit der Sicherheit in Zusammenhang stehen, z. B. das \_ ASC RET \_ ALLOCATED \_ MEMORY-Flag, können vor der endgültigen Rückgabe überprüft werden.

> [!Note]  
> Bestimmte Kontextattribute können sich während der Aushandlung mit einem Remotespeer ändern.

 

</dd> <dt>

*ptsExpiry* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in ortslokaler Zeit zurückgibt. Dieser Parameter ist optional, und **NULL** sollte für kurzlebige Clients übergeben werden.

Es gibt keine Ablaufzeit für Microsoft Digest [*SSP-Sicherheitskontexte*](../secgloss/s-gly.md)oder Anmeldeinformationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion einen der folgenden Erfolgscodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Der Client muss [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und dann die Ausgabe an den Server übergeben. Der Client wartet dann auf ein zurückgegebenes Token und übergibt es in einem anderen Aufruf an [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md).<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Der Client muss die Erstellung der Nachricht abschließen und dann die [**CompleteAuthToken-Funktion**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Der Client muss das Ausgabetoken an den Server senden und auf ein Rückgabetoken warten. Das zurückgegebene Token wird dann in einem anderen Aufruf von [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md)übergeben. Das Ausgabetoken kann leer sein.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Verwenden Sie mit Schannel. Der Server hat die Clientauthentifizierung angefordert, und die angegebenen Anmeldeinformationen enthalten entweder kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, die vom Server als vertrauenswürdig eingestuft wird. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                              |
| <dl> <dt>**SEC \_ E \_ INCOMPLETE \_ MESSAGE**</dt> </dl>     | Verwenden Sie mit Schannel. Daten für die gesamte Nachricht wurden nicht aus der Leitung gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pInput-Puffer* eine [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) mit einem **BufferType-Member** von **SECBUFFER \_ MISSING**. Der **cbBuffer-Member** von **SecBuffer** enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann sie die Leistung verbessern, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Der [*Sicherheitskontext*](../secgloss/s-gly.md) wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext(General)-Aufruf**](initializesecuritycontext--general.md) erforderlich. Wenn die Funktion ein Ausgabetoken zurückgibt, d. h., wenn das \_ SECBUFFER-TOKEN in *pOutput* eine Länge von ungleich 0 (null) hat, muss dieses Token an den Server gesendet werden.<br/>                                                                                                                                                    |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ INSUFFICIENT \_ MEMORY**</dt> </dl>          | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**\_INTERNER \_ SEC \_ E-FEHLER**</dt> </dl>               | Fehler, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>               | Das an die Funktion übergebene Handle ist ungültig.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ INVALID \_ TOKEN**</dt> </dl>                | Der Fehler ist auf ein falsch formatiertes Eingabetoken zurückzuführen, z. B. ein token beschädigt während der Übertragung, ein Token mit falscher Größe oder ein Token, das an das falsche [*Sicherheitspaket*](../secgloss/s-gly.md)übergeben wird. Die Übergabe eines Tokens an das falsche Paket kann auftreten, wenn Client und Server nicht das richtige Sicherheitspaket ausgehandelt [*haben.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | Fehler bei der Anmeldung.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | Für die Authentifizierung konnte keine Autorität kontaktiert werden. Der Domänenname der authentifizierenden Seite kann falsch sein, die Domäne kann nicht erreichbar sein, oder es ist ein Vertrauensstellungsfehler aufgetreten.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | Im [*Sicherheitspaket*](../secgloss/s-gly.md)sind keine Anmeldeinformationen verfügbar.<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ TARGET \_ UNKNOWN**</dt> </dl>               | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**\_NICHT \_ UNTERSTÜTZTE SEC \_ E-FUNKTION**</dt> </dl>         | Im fContextReq-Parameter wurde ein ungültiges Kontextattributflag \_ \_ (ISC REQ DELEGATE oder ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS) angegeben. <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>              | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *pszTargetName-Parameter übergeben* wurde. Dies weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort herunterfahren.

Wenn die Attribute des [*Sicherheitskontexts*](../secgloss/s-gly.md) nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) frei geben.

Die **InitializeSecurityContext(General)-Funktion** wird von einem Client verwendet, um einen ausgehenden Kontext zu initialisieren.

Für einen Zwei-Bein-Sicherheitskontext lautet die aufrufende Sequenz wie folgt: [](../secgloss/s-gly.md)

1.  Der Client ruft die Funktion auf, bei *der phContext* auf **NULL** festgelegt ist, und füllt den Pufferdeskriptor mit der Eingabenachricht auf.
2.  Das [*Sicherheitspaket*](../secgloss/s-gly.md) untersucht die Parameter und erstellt ein nicht transparentes Token und platziert es im TOKEN-Element im Pufferarray. Wenn der *fContextReq-Parameter* das ISC REQ ALLOCATE MEMORY-Flag enthält, weist das Sicherheitspaket den Arbeitsspeicher zu und gibt den Zeiger \_ im \_ \_ TOKEN-Element zurück. [](../secgloss/s-gly.md)
3.  Der Client sendet das im *pOutput-Puffer* zurückgegebene Token an den Zielserver. Der Server übergibt das Token dann als Eingabeargument in einem Aufruf der [**AcceptSecurityContext (General)-Funktion.**](acceptsecuritycontext--general.md)
4.  [**AcceptSecurityContext (Allgemein)**](acceptsecuritycontext--general.md) gibt möglicherweise ein Token zurück, das der Server für einen zweiten Aufruf von **InitializeSecurityContext (General)** an den Client sendet, wenn der erste Aufruf SEC I CONTINUE NEEDED zurückgegeben \_ \_ \_ hat.

Für Sicherheitskontexte mit [*mehreren*](../secgloss/s-gly.md)Beinen, z. B. gegenseitige Authentifizierung, lautet die aufrufende Sequenz wie folgt:

1.  Der Client ruft die Funktion wie zuvor beschrieben auf, aber das Paket gibt den Erfolgscode SEC \_ I \_ CONTINUE NEEDED \_ zurück.
2.  Der Client sendet das Ausgabetoken an den Server und wartet auf die Antwort des Servers.
3.  Nach Erhalt der Antwort des Servers ruft der Client **erneut InitializeSecurityContext (General)** auf, und *phContext* wird auf das Handle festgelegt, das vom letzten Aufruf zurückgegeben wurde. Das vom Server empfangene Token wird im *pInput-Parameter* angegeben.

Wenn der Server erfolgreich geantwortet hat, gibt [*das Sicherheitspaket*](../secgloss/s-gly.md) SEC \_ E OK \_ zurück, und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehlerantworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht eingerichtet.

Wenn die Funktion SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED oder SEC I COMPLETE AND CONTINUE zurückgibt, werden die \_ \_ Schritte \_ \_ \_ \_ \_ \_ \_ \_ 2 und 3 wiederholt.

Zum [*Initialisieren*](../secgloss/s-gly.md)eines Sicherheitskontexts kann je nach zugrunde liegendem Authentifizierungsmechanismus und den im *fContextReq-Parameter* angegebenen Optionen mehr als ein Aufruf dieser Funktion erforderlich sein.

Die *Parameter fContextReq* und *pfContextAttributes sind* Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Der *parameter pfContextAttributes* ist bei jeder erfolgreichen Rückgabe gültig, aber nur bei der endgültigen erfolgreichen Rückgabe sollten Sie die Flags untersuchen, die sich auf Sicherheitsaspekte des Kontexts beziehen. Zwischenrück rückgaben können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

Wenn das ISC REQ USE SUPPLIED CREDS-Flag festgelegt ist, muss das Sicherheitspaket im pInput-Eingabepuffer nach einem \_ \_ \_ \_ SECBUFFER [](../secgloss/s-gly.md) \_ PKG \_ PARAMS-Puffertyp suchen.  Dies ist keine generische Lösung, ermöglicht aber eine starke Kopplung von Sicherheitspaket [*und*](../secgloss/s-gly.md) Anwendung, wenn dies angemessen ist.

Wenn ISC REQ ALLOCATE MEMORY angegeben wurde, muss der Aufrufer den Arbeitsspeicher durch Aufrufen der \_ \_ \_ [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) frei geben.

Beispielsweise könnte das Eingabetoken die Herausforderung eines LAN-Managers sein. In diesem Fall wäre das Ausgabetoken die NTLM-verschlüsselte Antwort auf die Abfrage.

Die Vom Client ausgeführte Aktion hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode SEC E OK ist, gibt es keinen zweiten \_ \_ **InitializeSecurityContext (General)-Aufruf,** und es wird keine Antwort vom Server erwartet. Wenn der Rückgabecode SEC I CONTINUE NEEDED ist, erwartet der Client ein Token als Antwort vom Server und übergibt es in einem zweiten Aufruf an \_ \_ \_ **InitializeSecurityContext (Allgemein).** Der SEC I COMPLETE NEEDED-Rückgabecode gibt an, dass der Client die Meldung fertig stellen und \_ \_ die \_ [**CompleteAuthToken-Funktion aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) muss. Der SEC \_ I \_ COMPLETE AND \_ \_ CONTINUE-Code enthält beide Aktionen.

Wenn **InitializeSecurityContext (General)** einen Erfolg beim ersten (oder nur) Aufruf zurückgibt, muss der Aufrufer schließlich die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) für das zurückgegebene Handle aufrufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungsaustauschs fehlschlägt.

Der Client kann **InitializeSecurityContext (Allgemein)** erneut aufrufen, nachdem er erfolgreich abgeschlossen wurde. Dies weist das [*Sicherheitspaket darauf*](../secgloss/s-gly.md) hin, dass eine erneute Authentifizierung gewünscht ist.

Aufrufer im Kernelmodus haben die folgenden [](../secgloss/u-gly.md) Unterschiede: Der Zielname ist eine Unicode-Zeichenfolge, die mit [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Arbeitsspeicher zugeordnet werden muss. sie darf nicht aus dem Pool zugeordnet werden. In *pInput* und *pOutput* übergebene und bereitgestellte Puffer müssen sich im virtuellen Speicher und nicht im Pool befindet.

Wenn die Funktion bei Verwendung des Schannel-SSP SEC I INCOMPLETE CREDENTIALS zurückgibt, überprüfen Sie, ob Sie ein gültiges und vertrauenswürdiges \_ \_ Zertifikat in Ihren \_ Anmeldeinformationen angegeben haben. Das Zertifikat wird beim Aufrufen der [**AcquireCredentialsHandle (General)-Funktion**](acquirecredentialshandle--general.md) angegeben. Das Zertifikat muss ein Clientauthentifizierungszertifikat sein, das von einer Zertifizierungsstelle ausgestellt wurde, die vom Server als vertrauenswürdig eingestuft wird. Um eine Liste der Vom Server vertrauenswürdigen Zertifizierungas zu erhalten, rufen Sie die [**QueryContextAttributes (General)-Funktion**](querycontextattributes--general.md) auf, und geben Sie das SECPKG \_ ATTR \_ ISSUER LIST \_ \_ EX-Attribut an.

Wenn Sie den Schannel-SSP verwenden, erstellt die Anwendung nach dem Erhalt eines Authentifizierungszertifikats von einer Zertifizierungsstelle, die vom Server als vertrauenswürdig eingestuft wird, neue Anmeldeinformationen, indem sie die [**AcquireCredentialsHandle (General)-Funktion**](acquirecredentialshandle--general.md) aufruft und **dann initializeSecurityContext (General)** erneut aufruft und die neuen Anmeldeinformationen im *parameter phCredential angibt.*

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **InitializeSecurityContextW** (Unicode) und **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Allgemein)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**AcquireCredentialsHandle (Allgemein)**](acquirecredentialshandle--general.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
