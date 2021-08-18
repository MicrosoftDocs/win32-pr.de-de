---
description: Initiiert den clientseitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) aus einem Anmeldeinformationshandle mithilfe der [*eingeschränkten Kerberos-Delegierung.*](../secgloss/s-gly.md)
ms.assetid: b5c968dc-9343-44ed-acbc-a89c58c14e4a
title: InitializeSecurityContext(Kerberos)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f2a88fd930e58be418afa9d508adf9cda73912a8c0c5ea6731c06af5ec41a997
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482600"
---
# <a name="initializesecuritycontext-kerberos-function"></a>InitializeSecurityContext-Funktion (Kerberos)

Die **Funktion InitializeSecurityContext (Kerberos)** initiiert den clientseitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) aus einem Anmeldeinformationshandle. Die -Funktion wird verwendet, um einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen der Clientanwendung und einem Remotespeer zu erstellen. **InitializeSecurityContext (Kerberos)** gibt ein Token zurück, das der Client an den Remotespeer übergeben muss, den der Peer wiederum über den [**AcceptSecurityContext-Aufruf (Kerberos)**](acceptsecuritycontext--kerberos.md) an die lokale Sicherheitsimplementierungen übermittelt. Das generierte Token sollte von allen Aufrufern als nicht transparent betrachtet werden.

In der Regel wird die **Funktion InitializeSecurityContext (Kerberos)** in einer Schleife aufgerufen, bis ein ausreichender [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet ist.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_        SEC_CHAR       *pszTargetName,
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

Ein Handle für die anmeldeinformationen, die von [**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)zurückgegeben werden. Dieses Handle wird verwendet, um den [*Sicherheitskontext*](../secgloss/s-gly.md)zu erstellen. Die **Funktion InitializeSecurityContext (Kerberos)** erfordert mindestens OUTBOUND-Anmeldeinformationen.

</dd> <dt>

*phContext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Kerberos)** ist dieser Zeiger **NULL.** Beim zweiten Aufruf ist dieser Parameter ein Zeiger auf das Handle auf den teilweise gebildeten Kontext, der durch den ersten Aufruf im *phNewContext-Parameter* zurückgegeben wird.

</dd> <dt>

*pszTargetName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Dienstprinzipalnamen (Service Principal Name, SPN) oder den [*Sicherheitskontext*](../secgloss/s-gly.md) des Zielservers angibt.

Verwenden Sie einen vollqualifizierten Zielnamen, da Kurznamen nicht gesamtstrukturübergreifend unterstützt werden.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ \_ REQ, z. B. ISC \_ REQ \_ DELEGATE. Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Das [*Sicherheitspaket*](../secgloss/s-gly.md) ordnet Ihnen Ausgabepuffer zu. Wenn Sie die Verwendung der Ausgabepuffer abgeschlossen haben, können Sie sie freigeben, indem Sie die Funktion<strong>[FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Verschlüsseln Sie Nachrichten mithilfe der Funktion<strong>[EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen. Dieser Wert ist die Standardeinstellung.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Der Server kann den Kontext verwenden, um sich bei anderen Servern als Client zu authentifizieren. Das ISC_REQ_MUTUAL_AUTH-Flag muss festgelegt werden, damit dieses Flag funktioniert. Gültig für Kerberos. Ignorieren Sie dieses Flag für [*die eingeschränkte Delegierung.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Wenn Fehler auftreten, wird die Remotepartei benachrichtigt.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Signieren Sie Nachrichten, und überprüfen Sie Signaturen mithilfe der Funktionen [<strong>EncryptMessage</strong>](encryptmessage--general.md) und [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Die gegenseitige Authentifizierungsrichtlinie des Diensts wird erfüllt.<br/><blockquote>[!Caution]<br />
Dies bedeutet nicht unbedingt, dass die gegenseitige Authentifizierung ausgeführt wird, sondern nur, dass die Authentifizierungsrichtlinie des Diensts erfüllt ist. Um sicherzustellen, dass die gegenseitige Authentifizierung durchgeführt wird, rufen Sie die Funktion<strong>[QueryContextAttributes (Kerberos)</strong>](querycontextattributes--kerberos.md) auf.</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Wenn dieses Flag festgelegt ist, wird das <strong>ISC_REQ_INTEGRITY-Flag</strong> ignoriert.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Erkennen sie wiedergegebene Nachrichten, die mithilfe der Funktionen [<strong>EncryptMessage</strong>](encryptmessage--general.md) oder [<strong>MakeSignature</strong>](makesignature.md) codiert wurden.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Unterstützung einer streamorientierten Verbindung.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Ein neuer [*Sitzungsschlüssel*](../secgloss/s-gly.md) muss ausgehandelt werden.<br/></td></tr></tbody></table>



 

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

</dd> <dt>

*Reserviert1* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

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

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Kerberos)** empfängt dieser Zeiger das neue Kontexthandle. Beim zweiten Aufruf kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) enthält, die die Ausgabedaten empfängt. Wenn ein Puffer in der Eingabe als SEC \_ READWRITE eingegeben wurde, ist er bei der Ausgabe vorhanden. Das System ordnet auf Anforderung (über ISC REQ ALLOCATE MEMORY) einen Puffer für das Sicherheitstoken zu \_ und füllt die Adresse im \_ \_ Pufferdeskriptor für das Sicherheitstoken aus.

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

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurückgibt. Da dieser Parameter optional ist, sollte **NULL** für kurzlebige Clients übergeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion einen der folgenden Erfolgscodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Der [*Sicherheitskontext*](../secgloss/s-gly.md) wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext-Aufruf (Kerberos)**](initializesecuritycontext--kerberos.md) erforderlich. Wenn die Funktion ein Ausgabetoken zurückgibt, d. h., wenn das \_ SECBUFFER-TOKEN in *pOutput* eine Länge von ungleich 0 (null) hat, muss dieses Token an den Server gesendet werden.<br/> |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Der Client muss [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und dann die Ausgabe an den Server übergeben. Der Client wartet dann auf ein zurückgegebenes Token und übergibt es in einem anderen Aufruf an [**InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md)<br/>                                                                                                                                  |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Der Client muss die Erstellung der Nachricht abschließen und dann die [**CompleteAuthToken-Funktion**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/>                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Der Client muss das Ausgabetoken an den Server senden und auf ein Rückgabetoken warten. Das zurückgegebene Token wird dann in einem anderen Aufruf von [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)übergeben. Das Ausgabetoken kann leer sein.<br/>                                                                                                                                                       |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Verwenden Sie mit Schannel. Der Server hat die Clientauthentifizierung angefordert, und die angegebenen Anmeldeinformationen enthalten entweder kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, die dem Server vertraut. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ INSUFFICIENT \_ MEMORY**</dt> </dl>          | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**\_INTERNER \_ SEC \_ E-FEHLER**</dt> </dl>               | Fehler, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>               | Das an die Funktion übergebene Handle ist ungültig.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ INVALID \_ TOKEN**</dt> </dl>                | Der Fehler ist auf ein falsch formatiertes Eingabetoken zurückzuführen, z. B. auf ein während der Übertragung beschädigtes Token, ein Token mit falscher Größe oder ein Token, das an die falsche [*eingeschränkte Delegierung*](../secgloss/s-gly.md)übergeben wird. Die Übergabe eines Tokens an das falsche Paket kann auftreten, wenn client und server die ordnungsgemäße [*eingeschränkte Delegierung*](../secgloss/s-gly.md)nicht ausgehandelt haben.<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | Fehler bei der Anmeldung.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | Für die Authentifizierung konnte keine Autorität kontaktiert werden. Der Domänenname der authentifizierenden Seite kann falsch sein, die Domäne kann nicht erreichbar sein, oder es ist ein Vertrauensstellungsfehler aufgetreten.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmeldeinformationen verfügbar.<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ TARGET \_ UNKNOWN**</dt> </dl>               | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**\_NICHT \_ UNTERSTÜTZTE SEC \_ E-FUNKTION**</dt> </dl>         | Im fContextReq-Parameter wurde ein ungültiges Kontextattributflag \_ \_ (ISC REQ DELEGATE oder ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS) angegeben. <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>              | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht identisch mit dem Prinzipal, der an den *parameter pszTargetName* übergeben wird. Dies weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichen. Wenn z. B. Vertraulichkeit angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden.

Wenn attribute des [*Sicherheitskontexts*](../secgloss/s-gly.md) nicht ausreichen, muss der Client den teilweise erstellten Kontext freigeben, indem er die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) aufruft.

Die **Funktion InitializeSecurityContext (Kerberos)** wird von einem Client verwendet, um einen ausgehenden Kontext zu initialisieren.

Für einen zweistufigen [*Sicherheitskontext*](../secgloss/s-gly.md)sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client ruft die Funktion auf, wobei *phContext* auf **NULL** festgelegt ist, und füllt den Pufferdeskriptor mit der Eingabenachricht aus.
2.  Das [*Sicherheitspaket*](../secgloss/s-gly.md) untersucht die Parameter und erstellt ein nicht transparentes Token und platziert es im TOKEN-Element im Pufferarray. Wenn der *fContextReq-Parameter* das ISC \_ REQ \_ ALLOCATE \_ MEMORY-Flag enthält, ordnet das [*Sicherheitspaket*](../secgloss/s-gly.md) den Arbeitsspeicher zu und gibt den Zeiger im TOKEN-Element zurück.
3.  Der Client sendet das im *pOutput-Puffer* zurückgegebene Token an den Zielserver. Der Server übergibt dann das Token als Eingabeargument in einem Aufruf der [**AcceptSecurityContext (Kerberos)-Funktion.**](acceptsecuritycontext--kerberos.md)
4.  [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) gibt möglicherweise ein Token zurück, das der Server für einen zweiten Aufruf von **InitializeSecurityContext (Kerberos)** an den Client sendet, wenn der erste Aufruf SEC I CONTINUE NEEDED zurückgegeben \_ \_ \_ hat.

Für mehrstufige [*Sicherheitskontexte,*](../secgloss/s-gly.md)z. B. gegenseitige Authentifizierung, sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client ruft die Funktion wie zuvor beschrieben auf, aber das Paket gibt den Erfolgscode SEC \_ I CONTINUE \_ NEEDED \_ zurück.
2.  Der Client sendet das Ausgabetoken an den Server und wartet auf die Antwort des Servers.
3.  Nach Erhalt der Antwort des Servers ruft der Client **erneut InitializeSecurityContext (Kerberos)** auf, wobei *phContext* auf das Handle festgelegt ist, das vom letzten Aufruf zurückgegeben wurde. Das vom Server empfangene Token wird im *pInput-Parameter* bereitgestellt.

Wenn der Server erfolgreich geantwortet hat, gibt das [*Sicherheitspaket*](../secgloss/s-gly.md) SEC \_ E OK \_ zurück, und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehlerantworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht eingerichtet.

Wenn die Funktion SEC \_ I \_ CONTINUE NEEDED, SEC I COMPLETE NEEDED oder SEC I COMPLETE AND CONTINUE zurückgibt, werden die \_ Schritte \_ \_ \_ \_ \_ \_ \_ 2 und 3 wiederholt.

Zum Initialisieren eines [*Sicherheitskontexts*](../secgloss/s-gly.md)sind abhängig vom zugrunde liegenden Authentifizierungsmechanismus und den im *fContextReq-Parameter* angegebenen Optionen möglicherweise mehr als ein Aufruf dieser Funktion erforderlich.

Die Parameter *fContextReq* und *pfContextAttributes* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Der *pfContextAttributes-Parameter* ist bei jeder erfolgreichen Rückgabe gültig, aber nur bei der endgültigen erfolgreichen Rückgabe sollten Sie die Flags untersuchen, die sicherheitsaspekte des Kontexts betreffen. Zwischenrücksetzungen können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

Wenn das ISC \_ REQ \_ USE \_ SUPPLIED \_ CREDS-Flag festgelegt ist, muss das [*Sicherheitspaket*](../secgloss/s-gly.md) nach einem SECBUFFER \_ PKG \_ PARAMS-Puffertyp im *pInput-Eingabepuffer* suchen. Dies ist keine generische Lösung, ermöglicht aber ggf. eine starke Kopplung von [*Sicherheitspaket*](../secgloss/s-gly.md) und Anwendung.

Wenn ISC \_ REQ \_ ALLOCATE MEMORY angegeben \_ wurde, muss der Aufrufer den Arbeitsspeicher freigeben, indem er die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufruft.

Das Eingabetoken kann z. B. die Herausforderung eines LAN-Managers sein. In diesem Fall ist das Ausgabetoken die NTLM-verschlüsselte Antwort auf die Abfrage.

Die Aktion, die der Client vornimmt, hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode SEC \_ E \_ OK lautet, erfolgt kein zweiter **InitializeSecurityContext-Aufruf (Kerberos),** und es wird keine Antwort vom Server erwartet. Wenn der Rückgabecode SEC \_ I \_ CONTINUE NEEDED \_ lautet, erwartet der Client ein Token als Antwort vom Server und übergibt es in einem zweiten Aufruf an **InitializeSecurityContext (Kerberos).** Der \_ SEC I \_ COMPLETE \_ NEEDED-Rückgabecode gibt an, dass der Client die Erstellung der Nachricht abschließen und die [**CompleteAuthToken-Funktion**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen muss. Der \_ SEC I \_ COMPLETE AND \_ \_ CONTINUE-Code umfasst beide Aktionen.

Wenn **InitializeSecurityContext (Kerberos)** beim ersten (oder nur) Aufruf erfolglos zurückgibt, muss der Aufrufer schließlich die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) für das zurückgegebene Handle aufrufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungsaustauschs fehlschlägt.

Der Client kann **InitializeSecurityContext (Kerberos)** erneut aufrufen, nachdem er erfolgreich abgeschlossen wurde. Dies gibt dem [*Sicherheitspaket*](../secgloss/s-gly.md) an, dass eine erneute Authentifizierung gewünscht ist.

Kernelmodusaufrufer weisen die folgenden Unterschiede auf: Der Zielname ist eine [*Unicode-Zeichenfolge,*](../secgloss/u-gly.md) die mit [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Speicher zugeordnet werden muss. er darf nicht aus dem Pool zugeordnet werden. Puffer, die in *pInput* und *pOutput* übergeben und bereitgestellt werden, müssen sich im virtuellen Speicher und nicht im Pool befinden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)
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

 

 
