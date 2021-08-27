---
description: Initiiert den clientseitigen [](../secgloss/s-gly.md) ausgehenden Sicherheitskontext von einem Anmeldeinformationshandle mithilfe der eingeschränkten Schannel-Delegierung. [](../secgloss/s-gly.md)
ms.assetid: c451089a-d10d-469c-99dd-43d75a6b0b2a
title: InitializeSecurityContext-Funktion (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 29bbaeac3ef307e3ef846f526d96a98a22395742
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472906"
---
# <a name="initializesecuritycontext-schannel-function"></a>InitializeSecurityContext-Funktion (Schannel)

Die **InitializeSecurityContext-Funktion (Schannel)** initiiert den [](../secgloss/s-gly.md) clientseitigen ausgehenden Sicherheitskontext von einem Anmeldeinformationshandle. Die -Funktion wird verwendet, um einen [*Sicherheitskontext zwischen*](../secgloss/s-gly.md) der Clientanwendung und einem Remote-Peer zu erstellen. **InitializeSecurityContext (Schannel)** gibt ein Token zurück, das der Client an den Remote-Peer übergeben muss, den der Peer wiederum über den [**AcceptSecurityContext-Aufruf (Schannel)**](acceptsecuritycontext--schannel.md) an die lokale Sicherheitsimplementierung übermittelt. Das generierte Token sollte von allen Aufrufern als nicht transparent betrachtet werden.

In der Regel wird die **InitializeSecurityContext-Funktion (Schannel)** in einer Schleife aufgerufen, bis ein ausreichender [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wird.

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

Ein Handle für die Anmeldeinformationen, die [**von AcquireCredentialsHandle (Schannel) zurückgegeben werden.**](acquirecredentialshandle--schannel.md) Dieses Handle wird verwendet, um den [*Sicherheitskontext zu erstellen.*](../secgloss/s-gly.md) Die **InitializeSecurityContext-Funktion (Schannel)** erfordert mindestens OUTBOUND-Anmeldeinformationen.

</dd> <dt>

*phContext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Schannel)** ist dieser Zeiger **NULL.** Beim zweiten Aufruf ist dieser Parameter ein Zeiger auf das Handle auf den teilweise gebildeten Kontext, der durch den ersten Aufruf im *phNewContext-Parameter* zurückgegeben wird.

Geben Sie beim ersten Aufruf von **InitializeSecurityContext (Schannel)** **NULL an.** Geben Sie bei zukünftigen Aufrufen das Token an, das nach dem ersten Aufruf dieser Funktion im *parameter phNewContext* empfangen wurde.

</dd> <dt>

*pszTargetName* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Zielserver eindeutig identifiziert. Schannel verwendet diesen Wert, um das Serverzertifikat zu überprüfen. Schannel verwendet diesen Wert auch, um die Sitzung beim Wiederherstellen einer Verbindung im Sitzungscache zu suchen. Die zwischengespeicherte Sitzung wird nur verwendet, wenn alle der folgenden Bedingungen erfüllt sind:

-   Der Zielname ist identisch.
-   Der Cacheeintrag ist nicht abgelaufen.
-   Der Anwendungsprozess, der die Funktion aufruft, ist identisch.
-   Die Anmeldesitzung ist identisch.
-   Das Handle für Anmeldeinformationen ist identisch.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC REQ, z. \_ \_ B. ISC \_ REQ \_ DELEGATE. Dieser Parameter kann mindestens eines der folgenden Attributflags sein.




| Wert | Bedeutung | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | Das [*Sicherheitspaket*](../secgloss/s-gly.md) ordnet Ausgabepuffer für Sie zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie sie frei, indem Sie die [<strong>FreeContextBuffer-Funktion</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | Verschlüsseln Sie Nachrichten mithilfe der [<strong>EncryptMessage-Funktion.</strong>](encryptmessage--general.md)<br /> | 
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl><dt><strong>ISC_REQ_CONNECTION</strong></dt></dl> | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | Wenn Fehler auftreten, wird die Remote-Partei benachrichtigt.<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | Signieren Sie Nachrichten, und überprüfen Sie Signaturen mithilfe der [<strong>Funktionen EncryptMessage</strong>](encryptmessage--general.md) und [<strong>MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl><dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt></dl> | Schannel darf den Server nicht automatisch authentifizieren.<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | Die Richtlinie für gegenseitige Authentifizierung des Diensts wird erfüllt.<br /><blockquote>[!Caution]<br />Dies bedeutet nicht notwendigerweise, dass die gegenseitige Authentifizierung erfolgt, sondern nur, dass die Authentifizierungsrichtlinie des Diensts erfüllt ist. Um sicherzustellen, dass gegenseitige Authentifizierung erfolgt, rufen Sie die [<strong>Funktion QueryContextAttributes (Schannel)</strong>](querycontextattributes--schannel.md) auf.</blockquote><br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | Erkennen von wiedergegebenen Nachrichten, die mithilfe der [<strong>Funktionen EncryptMessage</strong>](encryptmessage--general.md) oder [<strong>MakeSignature codiert</strong>](makesignature.md) wurden.<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | Erkennen von Nachrichten, die nicht sequenziert empfangen werden.<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | Unterstützt eine streamorientierte Verbindung.<br /> | 
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl><dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt></dl> | Schannel darf nicht versuchen, Anmeldeinformationen für den Client automatisch anzugeben.<br /> | 




 

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *parameter pfContextAttr.*

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

</dd> <dt>

*Reserviert1* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht mit Schannel verwendet. Legen Sie sie auf 0 (null) fest.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Sofern der Clientkontext nicht vom Server initiiert wurde, muss der Wert dieses Parameters beim ersten Aufruf der Funktion **NULL** sein. Bei nachfolgenden Aufrufen der Funktion oder wenn der Clientkontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der mit genügend Arbeitsspeicher zum Speichern des vom Remotecomputer zurückgegebenen Tokens zugeordnet ist.

Bei Aufrufen dieser Funktion nach dem ersten Aufruf müssen zwei Puffer verwendet werden. Die erste hat den Typ **SECBUFFER \_ TOKEN** und enthält das vom Server empfangene Token. Der zweite Puffer hat den Typ **SECBUFFER \_ EMPTY.** Legen Sie sowohl den **pvBuffer-** als auch **den cbBuffer-Member** auf 0 fest.

</dd> <dt>

*Reserved2* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (Schannel)** empfängt dieser Zeiger das neue Kontexthandle. Beim zweiten Aufruf kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

Übergeben Sie bei Aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phContext-Parameter,* und geben Sie **NULL** für *phNewContext an.*

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) enthält, die die Ausgabedaten empfängt. Wenn ein Puffer in der Eingabe als SEC \_ READWRITE eingegeben wurde, ist er in der Ausgabe vorhanden. Das System ordnet bei Eineranforderung (über ISC REQ ALLOCATE MEMORY) einen Puffer für das Sicherheitstoken zu und füllt die Adresse im Pufferdeskriptor für das \_ \_ \_ Sicherheitstoken aus.

Wenn das ISC REQ ALLOCATE MEMORY-Flag angegeben ist, ordnet der Schannel-SSP Arbeitsspeicher für den Puffer zu und gibt die entsprechenden Informationen \_ \_ in \_ [**secBufferDesc ab.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Darüber hinaus muss der Aufrufer einen Puffer vom Typ **SECBUFFER \_ ALERT übergeben.** Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, um einen Satz von Bitflags zu empfangen, die die Attribute des eingerichteten [*Kontexts*](../secgloss/a-gly.md#_security_attribute_gly) angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

Flags, die für diesen Parameter verwendet werden, wird ISC \_ RET vorangestellt, z. B. ISC \_ RET \_ DELEGATE. Eine Liste der gültigen Werte finden Sie unter *dem fContextReq-Parameter.*

Überprüfen Sie erst nach sicherheitsbezogenen Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wird. Attributflags, die sich nicht auf die Sicherheit bezieht, z. B. das ASC \_ RET ALLOCATED MEMORY-Flag, können vor der \_ \_ endgültigen Rückgabe überprüft werden.

> [!Note]  
> Bestimmte Kontextattribute können sich während der Aushandlung mit einem Remote-Peer ändern.

 

</dd> <dt>

*ptsExpiry* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass [*das Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurück gibt. Dieser Parameter ist optional, und **NULL** sollte für kurzlebige Clients übergeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion einen der folgenden Erfolgscodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Der Client muss [**CompleteAuthToken aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) und dann die Ausgabe an den Server übergeben. Der Client wartet dann auf ein zurückgegebenes Token und übergibt es in einem anderen Aufruf an [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)<br/>                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Der Client muss die Meldung fertig stellen und dann die [**CompleteAuthToken-Funktion**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Der Client muss das Ausgabetoken an den Server senden und auf ein Rückgabetoken warten. Das zurückgegebene Token wird dann in einem anderen Aufruf von [**InitializeSecurityContext (Schannel) übergeben.**](initializesecuritycontext--schannel.md) Das Ausgabetoken kann leer sein.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Der Server hat die Clientauthentifizierung angefordert, und die angegebenen Anmeldeinformationen enthalten entweder kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, die vom Server als vertrauenswürdig eingestuft wird. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                         |
| <dl> <dt>**SEC \_ E \_ UNVOLLSTÄNDIGE \_ NACHRICHT**</dt> </dl>     | Daten für die gesamte Nachricht wurden nicht aus dem Netzwerk gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pInput-Puffer* eine [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) mit einem **BufferType-Member** **von SECBUFFER \_ MISSING**. Der **cbBuffer-Member** von **SecBuffer** enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion aus dem Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann ihre Verwendung zur Verbesserung der Leistung beitragen, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Der [*Sicherheitskontext*](../secgloss/s-gly.md) wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext-Aufruf (Schannel)**](initializesecuritycontext--schannel.md) erforderlich. Wenn die Funktion ein Ausgabetoken zurückgibt, das heißt, wenn das SECBUFFER-TOKEN in pOutput eine Länge ungleich \_ 0 (null) hat, muss dieses Token an den Server gesendet werden. <br/>                                                                                                                               |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_S.E \_ NICHT GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>            | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**INTERNER \_ FEHLER IN SEKUNDE E \_ \_**</dt> </dl>                 | Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>                 | Das an die Funktion übergebene Handle ist ungültig.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ TOKEN**</dt> </dl>                  | Der Fehler wird durch ein falsch formatiertes Eingabetoken verursacht, z. B. ein während der Übertragung beschädigtes Token, ein Token mit falscher Größe oder ein Token, das an die falsche eingeschränkte Delegierung [*übergeben wird.*](../secgloss/s-gly.md) Die Übergabe eines Tokens an das falsche Paket kann passieren, wenn client und server nicht die richtige [*eingeschränkte Delegierung aushandelt haben.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                   | Fehler bei der Anmeldung.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC E NO AUTHENTICATING AUTHORITY (KEINE \_ \_ \_ \_ AUTHENTIFIZIERUNGSSTELLE)**</dt> </dl>   | Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Der Domänenname der authentifizierenden Partei kann falsch sein, die Domäne kann nicht erreichbar sein, oder es ist ein Vertrauensstellungsfehler vor worden.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>                 | In der eingeschränkten Delegierung sind [*keine Anmeldeinformationen verfügbar.*](../secgloss/s-gly.md)<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ TARGET \_ UNKNOWN**</dt> </dl>                 | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E NICHT UNTERSTÜTZTE \_ \_ FUNKTION**</dt> </dl>           | Ein ungültiges Kontextattributflag (ISC \_ REQ \_ DELEGATE oder ISC \_ REQ PROMPT FOR \_ \_ CREDS) wurde im \_ *fContextReq-Parameter* angegeben.<br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>                | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *pszTargetName-Parameter übergeben* wurde. Dies weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                                          |
| <dl> <dt>**SEC \_ E \_ APPLICATION \_ PROTOCOL \_ MISMATCH**</dt> </dl> | Zwischen dem Client und dem Server ist kein gemeinsames Anwendungsprotokoll vorhanden.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort herunterfahren.

Wenn die Attribute des [*Sicherheitskontexts*](../secgloss/s-gly.md) nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) frei geben.

Die **InitializeSecurityContext-Funktion (Schannel)** wird von einem Client verwendet, um einen ausgehenden Kontext zu initialisieren.

Für einen Zwei-Bein-Sicherheitskontext lautet die aufrufende Sequenz wie folgt: [](../secgloss/s-gly.md)

1.  Der Client ruft die Funktion auf, bei *der phContext* auf **NULL** festgelegt ist, und füllt den Pufferdeskriptor mit der Eingabenachricht auf.
2.  Das [*Sicherheitspaket*](../secgloss/s-gly.md) untersucht die Parameter und erstellt ein nicht transparentes Token und platziert es im TOKEN-Element im Pufferarray. Wenn der *fContextReq-Parameter* das ISC REQ ALLOCATE MEMORY-Flag enthält, weist das Sicherheitspaket den Arbeitsspeicher zu und gibt den Zeiger \_ im \_ \_ TOKEN-Element zurück. [](../secgloss/s-gly.md)
3.  Der Client sendet das im *pOutput-Puffer* zurückgegebene Token an den Zielserver. Der Server übergibt das Token dann als Eingabeargument in einem Aufruf der [**AcceptSecurityContext-Funktion (Schannel).**](acceptsecuritycontext--schannel.md)
4.  [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) gibt möglicherweise ein Token zurück, das der Server für einen zweiten Aufruf von **InitializeSecurityContext (Schannel)** an den Client sendet, wenn der erste Aufruf SEC I CONTINUE NEEDED zurückgegeben \_ \_ \_ hat.

Für Sicherheitskontexte mit [*mehreren*](../secgloss/s-gly.md)Beinen, z. B. gegenseitige Authentifizierung, lautet die aufrufende Sequenz wie folgt:

1.  Der Client ruft die Funktion wie zuvor beschrieben auf, aber das Paket gibt den Erfolgscode SEC \_ I \_ CONTINUE NEEDED \_ zurück.
2.  Der Client sendet das Ausgabetoken an den Server und wartet auf die Antwort des Servers.
3.  Nach Erhalt der Antwort des Servers ruft der Client **erneut InitializeSecurityContext (Schannel)** auf, und *phContext* wird auf das Handle festgelegt, das vom letzten Aufruf zurückgegeben wurde. Das vom Server empfangene Token wird im *pInput-Parameter* angegeben.

Wenn der Server erfolgreich geantwortet hat, gibt [*das Sicherheitspaket*](../secgloss/s-gly.md) SEC \_ E OK \_ zurück, und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehlerantworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht eingerichtet.

Wenn die Funktion SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED oder SEC I COMPLETE AND CONTINUE zurückgibt, werden die \_ \_ Schritte \_ \_ \_ \_ \_ \_ \_ \_ 2 und 3 wiederholt.

Zum [*Initialisieren*](../secgloss/s-gly.md)eines Sicherheitskontexts kann je nach zugrunde liegendem Authentifizierungsmechanismus und den im *fContextReq-Parameter* angegebenen Optionen mehr als ein Aufruf dieser Funktion erforderlich sein.

Die *Parameter fContextReq* und *pfContextAttributes sind* Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Der *parameter pfContextAttributes* ist bei jeder erfolgreichen Rückgabe gültig, aber nur bei der endgültigen erfolgreichen Rückgabe sollten Sie die Flags untersuchen, die sich auf Sicherheitsaspekte des Kontexts beziehen. Zwischenrück rückgaben können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

Wenn das ISC REQ USE SUPPLIED CREDS-Flag festgelegt ist, muss das Sicherheitspaket im pInput-Eingabepuffer nach einem \_ \_ \_ \_ SECBUFFER [](../secgloss/s-gly.md) \_ PKG \_ PARAMS-Puffertyp suchen.  Dies ist keine generische Lösung, ermöglicht aber eine starke Kopplung von Sicherheitspaket [*und*](../secgloss/s-gly.md) Anwendung, wenn dies angemessen ist.

Wenn ISC REQ ALLOCATE MEMORY angegeben wurde, muss der Aufrufer den Arbeitsspeicher durch Aufrufen der \_ \_ \_ [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) frei geben.

Beispielsweise könnte das Eingabetoken die Herausforderung eines LAN-Managers sein. In diesem Fall wäre das Ausgabetoken die NTLM-verschlüsselte Antwort auf die Abfrage.

Die Vom Client ausgeführte Aktion hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode SEC E OK ist, gibt es keinen zweiten \_ \_ **InitializeSecurityContext (Schannel)-Aufruf,** und es wird keine Antwort vom Server erwartet. Wenn der Rückgabecode SEC I CONTINUE NEEDED ist, erwartet der Client ein Token als Antwort vom Server und übergibt es in einem zweiten Aufruf an \_ \_ \_ **InitializeSecurityContext (Schannel).** Der SEC I COMPLETE NEEDED-Rückgabecode gibt an, dass der Client die Meldung fertig stellen und \_ \_ die \_ [**CompleteAuthToken-Funktion aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) muss. Der SEC \_ I \_ COMPLETE AND \_ \_ CONTINUE-Code enthält beide Aktionen.

Wenn **InitializeSecurityContext (Schannel)** einen Erfolg beim ersten (oder nur) Aufruf zurückgibt, muss der Aufrufer schließlich die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) für das zurückgegebene Handle aufrufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungsaustauschs fehlschlägt.

Der Client kann **InitializeSecurityContext (Schannel)** erneut aufrufen, nachdem er erfolgreich abgeschlossen wurde. Dies weist das [*Sicherheitspaket darauf*](../secgloss/s-gly.md) hin, dass eine erneute Authentifizierung gewünscht ist.

Aufrufer im Kernelmodus haben die folgenden [](../secgloss/u-gly.md) Unterschiede: Der Zielname ist eine Unicode-Zeichenfolge, die mit [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Arbeitsspeicher zugeordnet werden muss. sie darf nicht aus dem Pool zugeordnet werden. In *pInput* und *pOutput* übergebene und bereitgestellte Puffer müssen sich im virtuellen Speicher und nicht im Pool befindet.

Wenn die Funktion SEC \_ I \_ INCOMPLETE CREDENTIALS zurückgibt, überprüfen Sie, ob Sie ein gültiges und vertrauenswürdiges \_ Zertifikat in Ihren Anmeldeinformationen angegeben haben. Das Zertifikat wird beim Aufrufen der [**Funktion AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) angegeben. Das Zertifikat muss ein Clientauthentifizierungszertifikat sein, das von einer Zertifizierungsstelle ausgestellt wurde, die vom Server als vertrauenswürdig eingestuft wird. Um eine Liste der Vom Server vertrauenswürdigen Zertifizierungas zu erhalten, rufen Sie die [**Funktion QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) auf, und geben Sie das SECPKG \_ ATTR \_ ISSUER LIST \_ \_ EX-Attribut an.

Nachdem eine Clientanwendung ein Authentifizierungszertifikat von einer Zertifizierungsstelle empfangen hat, die vom Server als vertrauenswürdig eingestuft wird, erstellt die Anwendung neue Anmeldeinformationen, indem sie die [**Funktion AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) aufruft und **dann initializeSecurityContext (Schannel)** erneut aufruft und die neuen Anmeldeinformationen im *parameter phCredential* angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md)
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

 

 
