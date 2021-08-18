---
description: Initiiert den clientseitigen ausgehenden Sicherheitskontext aus einem Anmeldeinformationshandle.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: InitializeSecurityContext (CredSSP)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5ba38dd10552f90ecfcc5045b96edc5e62aff1f8a2beec0f2a728fc1f0be8c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015990"
---
# <a name="initializesecuritycontext-credssp-function"></a>InitializeSecurityContext-Funktion (CredSSP)

Die **InitializeSecurityContext(CredSSP)-Funktion** initiiert den clientseitigen ausgehenden Sicherheitskontext aus einem Anmeldeinformationshandle. Die Funktion erstellt einen Sicherheitskontext zwischen der Clientanwendung und einem Remotespeer. **InitializeSecurityContext (CredSSP)** gibt ein Token zurück, das der Client an den Remotepeer übergeben muss. der Peer sendet dieses Token wiederum über den [**Aufruf von AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) an die lokale Sicherheitsimplementierungen. Das generierte Token sollte von allen Aufrufern als nicht transparent betrachtet werden.

In der Regel wird die **Funktion InitializeSecurityContext (CredSSP)** in einer Schleife aufgerufen, bis ein ausreichender Sicherheitskontext eingerichtet ist.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phCredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmeldeinformationen, die von [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)zurückgegeben werden. Dieses Handle wird verwendet, um den Sicherheitskontext zu erstellen. Die **Funktion InitializeSecurityContext (CredSSP)** erfordert mindestens OUTBOUND-Anmeldeinformationen.

</dd> <dt>

*phContext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (CredSSP)** ist dieser Zeiger **NULL.** Beim zweiten Aufruf ist dieser Parameter ein Zeiger auf das Handle auf den teilweise gebildeten Kontext, der durch den ersten Aufruf im *phNewContext-Parameter* zurückgegeben wird.

Geben Sie beim ersten Aufruf von **InitializeSecurityContext (CredSSP)** **NULL** an. Geben Sie bei zukünftigen Aufrufen das Token an, das im *parameter phNewContext* nach dem ersten Aufruf dieser Funktion empfangen wird.

</dd> <dt>

*pTargetName* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Zielserver eindeutig identifiziert. Schannel verwendet diesen Wert, um das Serverzertifikat zu überprüfen. Schannel verwendet diesen Wert auch, um die Sitzung im Sitzungscache zu suchen, wenn eine Verbindung wiederhergestellt wird. Die zwischengespeicherte Sitzung wird nur verwendet, wenn alle der folgenden Bedingungen erfüllt sind:

-   Der Zielname ist identisch.
-   Der Cacheeintrag ist nicht abgelaufen.
-   Der Anwendungsprozess, der die Funktion aufruft, ist identisch.
-   Die Anmeldesitzung ist identisch.
-   Das Handle für Anmeldeinformationen ist identisch.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ \_ REQ, z. B. ISC \_ REQ \_ DELEGATE.

Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



| Wert                                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> <dt>0x100</dt> </dl>                         | Das Sicherheitspaket ordnet dem Aufrufer Ausgabepuffer zu. Wenn Sie die Verwendung der Ausgabepuffer abgeschlossen haben, können Sie sie freigeben, indem Sie die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ REQ \_ CONNECTION**</dt> <dt>0x800</dt> </dl>                                         | Der Sicherheitskontext verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ REQ \_ EXTENDED \_ ERROR**</dt> <dt>0x4000</dt> </dl>                           | Wenn Fehler auftreten, wird die Remotepartei benachrichtigt.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ REQ \_ MANUAL \_ CRED \_ VALIDATION**</dt> <dt>0x80000</dt> </dl> | Der Credential Security Support Provider (CredSSP) darf den Server nicht automatisch authentifizieren. Dieses Flag wird immer festgelegt, wenn CredSSP verwendet wird.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ REQ \_ SEQUENCE \_ DETECT**</dt> <dt>0x8</dt> </dl>                           | Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ REQ \_ STREAM**</dt> <dt>0x8000</dt> </dl>                                                    | Unterstützung einer streamorientierten Verbindung.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ REQ \_ USE \_ SUPPLIED \_ CREDS**</dt> <dt>0x80</dt> </dl>                | CredSSP darf nicht versuchen, Anmeldeinformationen für den Client automatisch anzugeben.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ REQ \_ DELEGATE**</dt> <dt>0x1</dt> </dl>                                                 | Gibt an, dass die Anmeldeinformationen des Benutzers an den Server delegiert werden sollen.<br/> Wenn dieses Flag nicht angegeben ist, wird ein leerer Satz von Anmeldeinformationen an den Server delegiert.<br/> **Windows Server 2008 und Windows Vista:** Dieses Flag ist erforderlich.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ REQ \_ MUTUAL \_ AUTH**</dt> <dt>0x2</dt> </dl>                                       | Gibt an, dass keine Serverauthentifizierung erforderlich ist. Delegierungsrichtlinien werden weiterhin erzwungen, wenn dieses Flag nicht angegeben ist.<br/> **Windows Server 2008 und Windows Vista:** Dieses Flag wird ignoriert.<br/>                                                 |



 

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

</dd> <dt>

*Reserviert1* \[ In\]
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder **SECURITY \_ NATIVE \_ DREP** oder **SECURITY NETWORK \_ \_ DREP** sein.

</dd> <dt>

*pInput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Sofern der Clientkontext nicht vom Server initiiert wurde, muss der Wert dieses Parameters beim ersten Aufruf der Funktion **NULL** sein. Bei nachfolgenden Aufrufen der Funktion oder wenn der Clientkontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der mit genügend Arbeitsspeicher für das vom Remotecomputer zurückgegebene Token zugeordnet ist.

Bei Aufrufen dieser Funktion nach dem ersten Aufruf müssen zwei Puffer vorhanden sein. Der erste hat den Typ **SECBUFFER \_ TOKEN** und enthält das vom Server empfangene Token. Der zweite Puffer weist den Typ **SECBUFFER \_ EMPTY** auf. Legen Sie die **Member pvBuffer** und **cbBuffer** auf 0 (null) fest.

</dd> <dt>

*Reserviert2* \[ In\]
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **InitializeSecurityContext (CredSSP) empfängt** dieser Zeiger das neue Kontexthandle. Beim zweiten Aufruf kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

Übergeben Sie bei Aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phContext-Parameter,* und geben Sie **NULL** für *phNewContext an.*

</dd> <dt>

*pOutput* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Diese Struktur enthält wiederum Zeiger auf die [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Ausgabedaten empfängt. Wenn ein Puffer in der Eingabe als **SEC \_ READWRITE** eingegeben wurde, ist er bei der Ausgabe vorhanden. Das System ordnet auf Anforderung (über **ISC \_ REQ \_ ALLOCATE \_ MEMORY)** einen Puffer für das Sicherheitstoken zu und füllt die Adresse im Pufferdeskriptor für das Sicherheitstoken aus.

Wenn das **ISC \_ REQ \_ ALLOCATE \_ MEMORY-Flag** angegeben ist, belegt CredSSP Arbeitsspeicher für den Puffer und legt die entsprechenden Informationen in [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)ab.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Satz von Bitflags, die die [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ RET, z. B. **ISC \_ RET \_ DELEGATE**. Eine Liste gültiger Werte finden Sie im *fContextReq-Parameter.*

Suchen Sie erst nach sicherheitsrelevanten Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wurde. Attributflags, die nicht mit der Sicherheit in Zusammenhang stehen, z. B. das **ASC \_ RET \_ ALLOCATED \_ MEMORY-Flag,** können vor der endgültigen Rückgabe überprüft werden.

> [!Note]  
> Bestimmte Kontextattribute können sich während der Aushandlung mit einem Remotespeer ändern.

 

</dd> <dt>

*ptsExpiry* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das Sicherheitspaket diesen Wert immer in Ortszeit zurück gibt. Dieser Parameter ist optional, und **NULL** sollte für kurzlebige Clients übergeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie einen der folgenden Erfolgscodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ UNVOLLSTÄNDIGE \_ NACHRICHT**</dt> </dl>     | Daten für die gesamte Nachricht wurden nicht aus dem Netzwerk gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pInput-Puffer* eine [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) mit einem **BufferType-Member** **von SECBUFFER \_ MISSING**. Der **cbBuffer-Member** von **SecBuffer** gibt die Anzahl zusätzlicher Bytes an, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann ihre Verwendung zur Verbesserung der Leistung beitragen, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Der Sicherheitskontext wurde erfolgreich initialisiert. Ein weiterer [**InitializeSecurityContext-Aufruf (CredSSP)**](initializesecuritycontext--credssp.md) ist nicht erforderlich. If the function returns an output token -- that is, if the **SECBUFFER\_TOKEN** in *pOutput* is of nonzero length -- that token must be sent to the server.<br/>                                                                                                   |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Der Client muss [**CompleteAuthToken aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) und dann die Ausgabe an den Server übergeben. Der Client wartet dann auf ein zurückgegebenes Token und übergibt es in einem anderen Aufruf an [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Der Client muss die Meldung fertig stellen und dann die [**CompleteAuthToken-Funktion**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Der Client muss das Ausgabetoken an den Server senden und auf ein Rückgabetoken warten. Der Client übergibt das zurückgegebene Token in einem anderen Aufruf von [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Das Ausgabetoken kann leer sein.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Der Server hat die Clientauthentifizierung angefordert, aber entweder enthalten die angegebenen Anmeldeinformationen kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, der der Server vertraut. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                              |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_S.E \_ NICHT GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>          | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**INTERNER \_ FEHLER IN SEKUNDE E \_ \_**</dt> </dl>               | Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>               | Das an die Funktion übergebene Handle ist ungültig.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ TOKEN**</dt> </dl>                | Das Eingabetoken ist falsch formatiert. Mögliche Ursachen sind ein während der Übertragung beschädigtes Token, ein Token mit falscher Größe und ein Token, das an das falsche Sicherheitspaket übergeben wird. Diese letzte Bedingung kann vorkommen, wenn client und server nicht das richtige Sicherheitspaket aushandelt haben.<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | Fehler bei der Anmeldung.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC E NO AUTHENTICATING AUTHORITY (KEINE \_ \_ \_ \_ AUTHENTIFIZIERUNGSSTELLE)**</dt> </dl> | Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Der Domänenname der authentifizierenden Partei kann falsch sein, die Domäne kann nicht erreichbar sein, oder es ist ein Vertrauensstellungsfehler vor worden.<br/>                                                                    |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | Im Sicherheitspaket sind keine Anmeldeinformationen verfügbar.<br/>                                                                                                                                    |
| <dl> <dt>**SEC \_ E \_ TARGET \_ UNKNOWN**</dt> </dl>               | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E NICHT UNTERSTÜTZTE \_ \_ FUNKTION**</dt> </dl>         | Der Wert des *fContextReq-Parameters* ist ungültig. Entweder wurde kein erforderliches Flag angegeben, oder es wurde ein Flag angegeben, das von CredSSP nicht unterstützt wird.<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>              | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *pszTargetName-Parameter übergeben* wurde. Dieser Fehler weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                      |
| <dl> <dt>**SEC \_ \_ E-DELEGIERUNGSRICHTLINIE \_**</dt> </dl>            | Die Richtlinie unterstützt keine Delegierung von Anmeldeinformationen an den Zielserver.<br/>                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ POLICY \_ NLTM \_ ONLY**</dt> </dl>            | Die Delegierung von Anmeldeinformationen an den Zielserver ist nicht zulässig, wenn keine gegenseitige Authentifizierung erreicht wird.<br/>                                                                                                                                                                  |
| <dl> <dt>**SEC E MUTUAL AUTH FAILED (FEHLER BEI DER \_ \_ \_ GEGENSEITIGEN \_ AUTHENTIFIZIERUNG FÜR SEC E)**</dt> </dl>          | Fehler bei der Serverauthentifizierung, wenn das ISC \_ REQ \_ MUTUAL \_ AUTH-Flag im *fContextReq-Parameter angegeben* ist.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort herunterfahren.

Wenn die Attribute des Sicherheitskontexts nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) frei geben.

Der Client ruft die **Funktion InitializeSecurityContext (CredSSP)** auf, um einen ausgehenden Kontext zu initialisieren.

Bei einem Zwei-Bein-Sicherheitskontext lautet die aufrufende Sequenz wie folgt:

1.  Der Client ruft die Funktion auf, bei *der phContext* auf **NULL** festgelegt ist, und füllt den Pufferdeskriptor mit der Eingabenachricht auf.
2.  Das Sicherheitspaket untersucht die Parameter und erstellt ein nicht transparentes Token und platziert es im TOKEN-Element im Pufferarray. Wenn der *fContextReq-Parameter* das **ISC \_ REQ \_ ALLOCATE \_ MEMORY-Flag** enthält, weist das Sicherheitspaket den Arbeitsspeicher zu und gibt den Zeiger im TOKEN-Element zurück.
3.  Der Client sendet das im *pOutput-Puffer* zurückgegebene Token an den Zielserver. Der Server übergibt das Token dann als Eingabeargument in einem Aufruf der [**Funktion AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md)
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) gibt möglicherweise ein Token zurück. Der Server sendet dieses Token über einen zweiten **InitializeSecurityContext(CredSSP)-Aufruf an** den Client, wenn der erste Aufruf **SEC I CONTINUE NEEDED zurückgegeben \_ \_ \_ hat.**

Wenn der Server erfolgreich geantwortet hat, gibt das Sicherheitspaket **SEC \_ E OK \_ zurück,** und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehlerantworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht eingerichtet.

Wenn die Funktion **SEC \_ I CONTINUE \_ \_ NEEDED**, **SEC I COMPLETE \_ \_ \_ NEEDED** oder **SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE** zurückgibt, werden die Schritte 2 und 3 wiederholt.

Die Initialisierung des Sicherheitskontexts kann je nach zugrunde liegendem Authentifizierungsmechanismus und den im *fContextReq-Parameter* angegebenen Optionen mehrere Aufrufe dieser Funktion erfordern.

Die *Parameter fContextReq* und *pfContextAttributes sind* Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Obwohl der *parameter pfContextAttributes* bei jeder erfolgreichen Rückgabe gültig ist, sollten Sie die Flags, die sich auf Sicherheitsaspekte des Kontexts beziehen, nur bei der endgültigen erfolgreichen Rückgabe untersuchen. Zwischenrück rückgaben können z. B. das **ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag** festlegen.

Wenn das **ISC \_ REQ \_ USE SUPPLIED \_ \_ CREDS-Flag** festgelegt ist, muss das Sicherheitspaket im *pInput-Eingabepuffer* nach einem **SECBUFFER \_ PKG \_ PARAMS-Puffertyp** suchen. Obwohl dies keine generische Lösung ist, ermöglicht sie eine starke Kopplung von Sicherheitspaket und Anwendung, wenn dies angemessen ist.

Wenn **ISC \_ REQ \_ ALLOCATE \_ MEMORY** angegeben wurde, muss der Aufrufer den Arbeitsspeicher durch Aufrufen der [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) frei geben.

Beispielsweise könnte das Eingabetoken die Herausforderung eines LAN-Managers sein. In diesem Fall wäre das Ausgabetoken die NTLM-verschlüsselte Antwort auf die Abfrage.

Die Vom Client ausgeführte Aktion hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode **SEC \_ E OK \_ ist,** gibt es keinen zweiten **InitializeSecurityContext (CredSSP)-Aufruf,** und es wird keine Antwort vom Server erwartet. Wenn der Rückgabecode **SEC \_ I CONTINUE \_ \_ NEEDED** ist, erwartet der Client ein Token als Antwort vom Server und übergibt es in einem zweiten Aufruf an **InitializeSecurityContext (CredSSP).** Der **SEC I COMPLETE \_ \_ \_ NEEDED-Rückgabecode** gibt an, dass der Client die Meldung fertig stellen und die [**CompleteAuthToken-Funktion aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) muss. Der **SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE-Code** enthält beide Aktionen.

Wenn **InitializeSecurityContext (CredSSP)** einen Erfolg beim ersten (oder nur) Aufruf zurückgibt, muss der Aufrufer schließlich die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) für das zurückgegebene Handle aufrufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungsaustauschs fehlschlägt.

Der Client kann **InitializeSecurityContext (CredSSP)** erneut aufrufen, nachdem er erfolgreich abgeschlossen wurde. Dies weist das Sicherheitspaket darauf hin, dass eine erneute Authentifizierung gewünscht ist.

Aufrufer im Kernelmodus haben die folgenden Unterschiede: Der Zielname ist eine Unicode-Zeichenfolge, die mit [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Arbeitsspeicher zugeordnet werden muss. [](../secgloss/u-gly.md#_security_unicode_gly) sie darf nicht aus dem Pool zugeordnet werden. In *pInput* und *pOutput* übergebene und bereitgestellte Puffer müssen sich im virtuellen Speicher und nicht im Pool befindet.

Wenn die Funktion **SEC \_ I INCOMPLETE \_ \_ CREDENTIALS** zurückgibt, überprüfen Sie, ob die an die [**Funktion AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) übergebenen R-Anmeldeinformationen ein gültiges und vertrauenswürdiges Zertifikat angegeben haben. Das Zertifikat muss ein Clientauthentifizierungszertifikat sein, das von einer vom Server als vertrauenswürdig eingestuften Zertifizierungsstelle ausgestellt wurde. Um eine Liste der Vom Server vertrauenswürdigen Zertifizierungas zu erhalten, rufen Sie die [**Funktion QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) mit dem **SECPKG \_ ATTR \_ ISSUER LIST \_ \_ EX-Attribut** auf.

Nach dem Empfang eines Authentifizierungszertifikats von einer Zertifizierungsstelle, der der Server vertraut, erstellt die Clientanwendung neue Anmeldeinformationen. Rufen Sie dazu die [**Funktion AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) auf, und rufen Sie **dann erneut InitializeSecurityContext (CredSSP)** auf, und geben Sie dabei die neuen Anmeldeinformationen im *parameter phCredential* an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
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

 

 
