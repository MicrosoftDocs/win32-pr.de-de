---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten.
ms.assetid: eaa15fed-4438-4e43-9be3-aa100ca453c7
title: AcceptSecurityContext(General)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9e9bd29307179bb845c159b2427cbea807c607ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628702"
---
# <a name="acceptsecuritycontext-general-function"></a>AcceptSecurityContext(General)-Funktion

Die **AcceptSecurityContext (Allgemein)-Funktion** ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten. Der Remoteclient verwendet die [**InitializeSecurityContext (General)-Funktion,**](initializesecuritycontext--general.md) um den Prozess zum Einrichten eines [*Sicherheitskontexts*](../secgloss/s-gly.md)zu starten. Der Server kann mindestens ein Antworttoken vom Remoteclient anfordern, um die Einrichtung des [*Sicherheitskontexts*](../secgloss/s-gly.md)abzuschließen.

Informationen zur Verwendung dieser Funktion mit einem bestimmten [*Sicherheitssupportanbieter (Security Support Provider,*](../secgloss/s-gly.md) SSP) finden Sie in den folgenden Themen.



| Thema                                                                          | Beschreibung                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)     | Ermöglicht der Serverkomponente einer Transportanwendung die Einrichtung eines [*Sicherheitskontexts*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient mithilfe von Credential Security Support Provider (CredSSP).<br/> |
| [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)       | Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten, der Digest verwendet.<br/>                                                                                                                  |
| [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)   | Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten, der Kerberos verwendet.<br/>                                                                                                                |
| [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) | Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten, der Negotiate verwendet.<br/>                                                                                                               |
| [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)           | Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten, der NTLM verwendet.<br/>                                                                                                                    |
| [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)   | Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient herzustellen, der Schannel verwendet.<br/>                                                                                                                |



 

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
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phCredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmeldeinformationen des Servers. Der Server ruft die [**AcquireCredentialsHandle (General)-Funktion**](acquirecredentialshandle--general.md) auf, wobei entweder das SECPKG \_ CRED \_ INBOUND- oder SECPKG \_ CRED \_ BOTH-Flag festgelegt ist, um dieses Handle abzurufen.

</dd> <dt>

*phContext* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Allgemein)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen ist *phContext* das Handle für den teilweise gebildeten Kontext, der im *phNewContext-Parameter* durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (Allgemein)**](initializesecuritycontext--general.md) generiert wird und den Eingabepufferdeskriptor enthält.

Bei Verwendung des Schannel-SSP muss der erste Puffer vom Typ SECBUFFER TOKEN sein \_ und das vom Client empfangene Sicherheitstoken enthalten. Der zweite Puffer sollte vom Typ SECBUFFER \_ EMPTY sein.

Bei Verwendung der Negotiate-, Kerberos- oder NTLM-SSPs können Kanalbindungsinformationen durch Übergeben einer [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ **SECBUFFER \_ CHANNEL \_ BINDINGS** zusätzlich zu den Puffern angegeben werden, die durch den Aufruf der [**InitializeSecurityContext (General)-Funktion**](initializesecuritycontext--general.md) generiert werden. Die Kanalbindungsinformationen für den Kanalbindungspuffer können abgerufen werden, indem die [**QueryContextAttributes (Schannel)-Funktion**](querycontextattributes--schannel.md) für den Schannelkontext aufgerufen wird, den der Client für die Authentifizierung verwendet hat.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mit bitweisen **OR-Vorgängen** kombiniert werden. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> </dl>                                                  | Digest und Schannel ordnen Ausgabepuffer für Sie zu. Wenn Sie die Verwendung der Ausgabepuffer abgeschlossen haben, können Sie sie freigeben, indem Sie die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ REQ \_ ALLOW \_ MISSING \_ BINDINGS**</dt> </dl>                            | Gibt an, dass Digest keine Kanalbindungen für innere und äußere Kanäle erfordert. Dieser Wert wird aus Gründen der Abwärtskompatibilität verwendet, wenn die Unterstützung für die Endpunktkanalbindung nicht bekannt ist.<br/> Dieser Wert schließen sich mit **ASC \_ REQ PROXY BINDINGS gegenseitig \_ \_ aus.**<br/> Dieser Wert wird nur vom Digest-SSP unterstützt.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ REQ \_ CONFIDENTIALITY**</dt> </dl>                                                   | Verschlüsseln und Entschlüsseln von Nachrichten. <br/> Der Digest-SSP unterstützt dieses Flag nur für SASL.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ REQ \_ CONNECTION**</dt> </dl>                                                                  | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ REQ \_ DELEGATE**</dt> </dl>                                                                        | Der Server darf die Identität des Clients annehmen. Gültig für Kerberos. Ignorieren Sie dieses Flag für [*die eingeschränkte Delegierung.*](../secgloss/c-gly.md)<br/>                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ REQ \_ EXTENDED \_ ERROR**</dt> </dl>                                                     | Wenn Fehler auftreten, wird die Remotepartei benachrichtigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ REQ \_ HTTP (0x10000000)**</dt> </dl> | Verwenden Sie Digest für HTTP. Lassen Sie dieses Flag aus, um Digest als SASL-Mechanismus zu verwenden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ REQ \_ INTEGRITY**</dt> </dl>                                                                     | Signieren von Nachrichten und Überprüfen von Signaturen.<br/> Schannel unterstützt dieses Flag nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**ASC \_ REQ \_ MUTUAL \_ AUTH**</dt> </dl>                                                              | Der Client muss ein Zertifikat bereitstellen, das für die Clientauthentifizierung verwendet werden soll.<br/> Dieses Flag wird nur von Schannel unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**\_ \_ ASC-REQ-PROXYBINDUNGEN \_**</dt> </dl>                                                     | Gibt an, dass digest kanalbindung erfordert.<br/> Dieser Wert schließen sich mit **ASC \_ REQ ALLOW MISSING BINDINGS gegenseitig \_ \_ \_ aus.**<br/> Dieser Wert wird nur vom Digest-SSP unterstützt.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>                                                        | Erkennen wiedergegebener Pakete.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl>                                                  | Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**ASC \_ REQ \_ STREAM**</dt> </dl>                                                                              | Unterstützung einer streamorientierten Verbindung.<br/> Dieses Flag wird nur von Schannel unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |



 

Mögliche Attributflags und ihre Bedeutungen finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC \_ REQ, z. B. ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

Dieser Parameter wird nicht mit Schannel oder Digest-SSPs verwendet. Wenn Sie Schannel oder Digest-SSPs verwenden, geben Sie für diesen Parameter 0 (null) an.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Allgemein)** empfängt dieser Zeiger das neue Kontexthandle. Bei nachfolgenden Aufrufen kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (Allgemein)**](initializesecuritycontext--general.md)an den Client gesendet. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E OK zurückgibt. \_ Alle generierten Puffer müssen zurück an die Clientanwendung gesendet werden.

Bei Verwendung von Schannel empfängt dieser Puffer bei der Ausgabe ein Token für den [*Sicherheitskontext*](../secgloss/s-gly.md). Das Token muss an den Client gesendet werden. Die Funktion kann auch einen Puffer vom Typ SECBUFFER \_ EXTRA zurückgeben. Darüber hinaus muss der Aufrufer einen Puffer vom Typ **SECBUFFER \_ ALERT übergeben.** Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC RET, z. \_ B. ASC \_ RET \_ DELEGATE.

Überprüfen Sie erst nach sicherheitsbezogenen Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wird. Attributflags, die sich nicht auf die Sicherheit bezieht, z. B. das ASC \_ RET ALLOCATED MEMORY-Flag, können vor der \_ \_ endgültigen Rückgabe überprüft werden.

</dd> <dt>

*ptsTimeStamp* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, [*dass das Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurück gibt.

Dieser Parameter wird auf eine konstante maximale Zeit festgelegt. Es gibt keine Ablaufzeit für [*Digestsicherheitskontexte*](../secgloss/s-gly.md)oder Anmeldeinformationen oder bei Verwendung des Digest-SSP.

Dies ist optional, wenn Der Schannel-SSP verwendet wird. Wenn die Remote-Partei ein Zertifikat bereitgestellt hat, das für die Authentifizierung verwendet werden soll, erhält dieser Parameter die Ablaufzeit für dieses Zertifikat. Wenn kein Zertifikat angegeben wurde, wird ein maximaler Zeitwert zurückgegeben.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>Fehler bei der Funktion. Die Kanalbindungsrichtlinie wurde nicht erfüllt.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss zusätzliche Daten vom Client lesen und [<strong>AcceptSecurityContext (Allgemein)</strong>](acceptsecuritycontext--general.md) erneut aufrufen.<br/> Dieser Wert kann bei Verwendung des Schannel-SSP zurückgegeben werden. Weitere Informationen zu diesem Rückgabewert finden Sie unter [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Fehler bei der Funktion. Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Fehler bei der Anmeldung.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Fehler bei der Funktion. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann folgende Bedingungen haben:<br/><ul><li>Der Domänenname der authentifizierenden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Fehler bei der Funktion. Das im <em>phCredential-Parameter angegebene Anmeldeinformationshandl</em> ist ungültig. Dieser Wert kann bei Verwendung des Digest- oder Schannel-SSP zurückgegeben werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der [*vom Client*](../secgloss/s-gly.md) empfangene Sicherheitskontext wurde akzeptiert. Wenn ein Ausgabetoken von der Funktion generiert wurde, muss es an den Clientprozess gesendet werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>Fehler bei der Funktion. Im fContextReq-Parameter wurde ein ungültiges <em>Kontextattributflag</em> angegeben. Dieser Wert kann bei Verwendung des Digest-SSP zurückgegeben werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>Fehler bei der Funktion. Ein ungültiges Kontextattributflag (ASC_REQ_DELEGATE oder ASC_REQ_PROMPT_FOR_CREDS) wurde im <em>fContextReq-Parameter</em> angegeben. Dieser Wert kann bei Verwendung des Schannel-SSP zurückgegeben werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und das Ausgabetoken an den Client übergeben. Der Server wartet dann auf ein Rückgabetoken vom Client und führt dann einen weiteren Aufruf von [<strong>AcceptSecurityContext (General)</strong>](acceptsecuritycontext--general.md) aus. <br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Nachricht vom Client fertigstellen und dann die Funktion [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in <em>pInput für einen</em> weiteren Aufruf von [<strong>AcceptSecurityContext (General)</strong>](acceptsecuritycontext--general.md) übergeben werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Fehler bei der Funktion. Die<strong>[AcceptSecurityContext (General)</strong>](acceptsecuritycontext--general.md)-Funktion wurde aufgerufen, nachdem der angegebene Kontext eingerichtet wurde. Dieser Wert kann bei Verwendung des Digest-SSP zurückgegeben werden.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Hinweise

Die **AcceptSecurityContext(General)-Funktion** ist das Serverent pendant zur [**InitializeSecurityContext (General)-Funktion.**](initializesecuritycontext--general.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *Parameter fContextReq,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients [](../secgloss/i-gly.md)in der Lage sein müssen, eine vertrauliche oder integritätsgeprüfte Sitzung zu verwenden, und Clients ablehnen, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts benötigen, und alles, was der Client bereitstellen oder erfordert, wird im *parameter pfContextAttr zurückgegeben.*

Für ein Paket, das mehrseitige Authentifizierung unterstützt, z. B. gegenseitige Authentifizierung, lautet die aufrufende Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server ruft **AcceptSecurityContext (General)** zum ersten Mal auf, wodurch ein Antworttoken generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Allgemein).**](initializesecuritycontext--general.md) Wenn **InitializeSecurityContext (Allgemein)** SEC E OK zurückgibt, wurde die gegenseitige Authentifizierung \_ \_ abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Allgemein) einen** Fehlercode zurückgibt, wird die gegenseitige Authentifizierungsaushandlung beendet. Andernfalls wird das von **InitializeSecurityContext (Allgemein)** zurückgegebene Sicherheitstoken an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die *Parameter fContextReq* und *pfContextAttr* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

> [!Note]  
> Der *pfContextAttr-Parameter* ist bei jeder erfolgreichen Rückgabe gültig, aber nur bei der endgültigen erfolgreichen Rückgabe sollten Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts untersuchen. Zwischenrücksetzungen können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn z. B. Vertraulichkeit (Verschlüsselung) angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext freigeben, indem er die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) aufruft. Informationen dazu, wann die **DeleteSecurityContext-Funktion** aufgerufen werden soll, finden Sie unter **DeleteSecurityContext**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Clientzertifikat zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Benutzers zu annehmen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Allgemein)**](initializesecuritycontext--general.md)
</dt> </dl>

 

 
