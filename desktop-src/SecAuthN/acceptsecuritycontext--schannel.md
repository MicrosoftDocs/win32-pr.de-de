---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen Sicherheitskontext zwischen dem Server und einem Remoteclient herzustellen, der Schannel verwendet. [](../secgloss/s-gly.md)
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: AcceptSecurityContext-Funktion (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 2700704c9fc1c40fc2d5648306147c5091a318e5c8bd4383bb32bc5416c8d069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141643"
---
# <a name="acceptsecuritycontext-schannel-function"></a>AcceptSecurityContext-Funktion (Schannel)

Mit **der AcceptSecurityContext-Funktion (Schannel)** kann die Serverkomponente [](../secgloss/s-gly.md) einer Transportanwendung einen Sicherheitskontext zwischen dem Server und einem Remoteclient einrichten. Der Remoteclient verwendet die [**InitializeSecurityContext-Funktion (Schannel),**](initializesecuritycontext--schannel.md) um den Prozess zum Einrichten eines [*Sicherheitskontexts zu starten.*](../secgloss/s-gly.md) Der Server kann mindestens ein Antworttoken vom Remoteclient benötigen, um die Einrichtung des [*Sicherheitskontexts abschließen zu können.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsTimeStamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phCredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmeldeinformationen des Servers. Der Server ruft die [**AcquireCredentialsHandle(Schannel)-Funktion**](acquirecredentialshandle--schannel.md) auf, bei der entweder das SECPKG \_ CRED \_ INBOUND- oder SECPKG CRED BOTH-Flag festgelegt ist, um dieses Handle \_ \_ abzurufen.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Schannel)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen *ist phContext* das Handle für den teilweise gebildeten Kontext, der vom ersten Aufruf im *phNewContext-Parameter* zurückgegeben wurde.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) generiert wird, der den Eingabepufferdeskriptor enthält.

Bei Verwendung des Schannel-Sicherheitssupportanbieters (Security [*Support Provider,*](../secgloss/s-gly.md) SSP) muss der erste Puffer vom Typ SECBUFFER TOKEN sein und das vom Client empfangene \_ Sicherheitstoken enthalten. Der zweite Puffer muss vom Typ SECBUFFER \_ EMPTY sein.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mithilfe bitweiser **OR-Vorgänge kombiniert** werden. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ \_ REQ– SPEICHER \_ ZUWEISEN**</dt> </dl> | Digest und Schannel weisen Ausgabepuffer für Sie zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie sie frei, indem Sie die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ \_ REQ-VERTRAULICHKEIT**</dt> </dl>  | Verschlüsseln und Entschlüsseln von Nachrichten.<br/> Der Digest-SSP unterstützt dieses Flag nur für SASL.<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ \_ REQ-VERBINDUNG**</dt> </dl>                 | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERWEITERTER ASC \_ \_ \_ REQ-FEHLER**</dt> </dl>    | Wenn Fehler auftreten, wird die Remote-Partei benachrichtigt.<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**ASC \_ REQ \_ MUTUAL \_ AUTH**</dt> </dl>             | Der Client muss ein Zertifikat für die Clientauthentifizierung liefern.<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Erkennen von wiedergegebenen Paketen.<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Erkennen von Nachrichten, die nicht sequenziert empfangen werden.<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**ASC \_ REQ \_ STREAM**</dt> </dl>                             | Unterstützt eine streamorientierte Verbindung.<br/> Dieses Flag wird nur von Schannel unterstützt.<br/>                                                                                                    |



 

Mögliche Attributflags und deren Bedeutung finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC REQ, z. B. \_ ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *parameter pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Dieser Parameter wird nicht mit Schannel verwendet. Geben Sie 0 (null) für diesen Parameter an.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Schannel)** empfängt dieser Zeiger das neue Kontexthandle. Bei nachfolgenden Aufrufen *kann phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (Schannel) an den Client gesendet.**](initializesecuritycontext--schannel.md) Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E \_ OK zurückgibt. Alle generierten Puffer müssen zurück an die Clientanwendung gesendet werden.

Bei der Ausgabe empfängt dieser Puffer ein Token für den [*Sicherheitskontext*](../secgloss/s-gly.md). Das Token muss an den Client gesendet werden. Die Funktion kann auch einen Puffer vom Typ SECBUFFER \_ EXTRA zurückgeben. Darüber hinaus muss der Aufrufer einen Puffer vom Typ **SECBUFFER \_ ALERT übergeben.** Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC RET, z. \_ B. ASC \_ RET \_ DELEGATE.

Überprüfen Sie erst nach sicherheitsbezogenen Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wird. Attributflags, die sich nicht auf die Sicherheit bezieht, z. B. das ASC \_ RET ALLOCATED MEMORY-Flag, können vor der \_ \_ endgültigen Rückgabe überprüft werden.

</dd> <dt>

*ptsTimeStamp* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, [*dass das Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurück gibt.

Dies ist optional, wenn Der Schannel-SSP verwendet wird. Wenn die Remote-Partei ein Zertifikat bereitgestellt hat, das für die Authentifizierung verwendet werden soll, erhält dieser Parameter die Ablaufzeit für dieses Zertifikat. Wenn kein Zertifikat angegeben wurde, wird ein maximaler Zeitwert zurückgegeben.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss zusätzliche Daten vom Client lesen und [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md) erneut aufrufen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der <em>pInput-Puffer</em> eine [<strong>SecBuffer</strong>](/windows/win32/api/sspi/ns-sspi-secbuffer)-Struktur mit einem <strong>BufferType-Member</strong> <strong>SECBUFFER_MISSING.</strong> Der <strong>cbBuffer-Member</strong> von <strong>SecBuffer</strong> enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion aus dem Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann ihre Verwendung die Leistung verbessern, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Fehler bei der Funktion. Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Fehler bei der Anmeldung.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Fehler bei der Funktion. Für die Authentifizierung konnte keine Autorität kontaktiert werden. Dies kann auf die folgenden Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänenname der authentifizierenden Seite ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Fehler bei der Vertrauensstellung.</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Fehler bei der Funktion. Das im <em>phCredential-Parameter</em> angegebene Handle für Anmeldeinformationen ist ungültig. Dieser Wert kann bei Verwendung des Digest- oder Schannel-SSP zurückgegeben werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene [*Sicherheitskontext*](../secgloss/s-gly.md) wurde akzeptiert. Wenn ein Ausgabetoken von der Funktion generiert wurde, muss es an den Clientprozess gesendet werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>Fehler bei der Funktion. Im <em>fContextReq-Parameter</em> wurde ein ungültiges Kontextattributflag (ASC_REQ_DELEGATE oder ASC_REQ_PROMPT_FOR_CREDS) angegeben.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367L</dt> </dl></td><td>Zwischen dem Client und dem Server ist kein allgemeines Anwendungsprotokoll vorhanden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und das Ausgabetoken an den Client übergeben. Der Server wartet dann auf ein Rückgabetoken vom Client und ruft dann erneut [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md) auf. <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Erstellung der Nachricht vom Client abschließen und dann die Funktion<strong>[CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in <em>pInput</em> für einen weiteren Aufruf von [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md) übergeben werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Fehler bei der Funktion. Die Funktion [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md) wurde aufgerufen, nachdem der angegebene Kontext eingerichtet wurde. Dieser Wert kann bei Verwendung des Digest-SSP zurückgegeben werden.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Hinweise

Die **AcceptSecurityContext (Schannel)-Funktion** ist die Serverentsprechung zur [**InitializeSecurityContext (Schannel)-Funktion.**](initializesecuritycontext--schannel.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *fContextReq-Parameter,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients [](../secgloss/i-gly.md)eine vertrauliche oder integritätsüberprüfungsbasierte Sitzung verwenden müssen, und Clients ablehnen können, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts erfordern, und das, was der Client bereitstellen kann oder erfordert, wird im *pfContextAttr-Parameter* zurückgegeben.

Für ein Paket, das die mehrstufige Authentifizierung unterstützt, z. B. gegenseitige Authentifizierung, sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server ruft **AcceptSecurityContext (Schannel)** zum ersten Mal auf, wodurch ein Antworttoken generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Wenn **InitializeSecurityContext (Schannel)** SEC E OK zurückgibt, wurde die \_ gegenseitige \_ Authentifizierung abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Schannel)** einen Fehlercode zurückgibt, wird die gegenseitige Authentifizierungsaushandlung beendet. Andernfalls wird das von **InitializeSecurityContext (Schannel)** zurückgegebene Sicherheitstoken an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die Parameter *fContextReq* und *pfContextAttr* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

> [!Note]  
> Der *pfContextAttr-Parameter* ist bei jeder erfolgreichen Rückgabe gültig, jedoch nur bei der endgültigen erfolgreichen Rückgabe, wenn Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts untersuchen. Zwischenrücksetzungen können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichen. Wenn z. B. Vertraulichkeit (Verschlüsselung) angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext freigeben, indem er die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) aufruft. Informationen dazu, wann die **DeleteSecurityContext-Funktion** aufgerufen werden soll, finden Sie unter **DeleteSecurityContext**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Clientzertifikat zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Benutzers zu annehmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
