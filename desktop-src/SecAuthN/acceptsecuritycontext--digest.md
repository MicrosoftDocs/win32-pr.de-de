---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen Sicherheitskontext zwischen dem Server und einem Remoteclient einzurichten, der Digest verwendet.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: AcceptSecurityContext(Digest)-Funktion (Sspi.h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: ec6ad11e754124f56f5852b4e0b0a0347f1bb099
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628712"
---
# <a name="acceptsecuritycontext-digest-function"></a>AcceptSecurityContext-Funktion (Digest)

Mit der **AcceptSecurityContext-Funktion (Digest)** kann die Serverkomponente einer Transportanwendung einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einrichten. Der Remoteclient verwendet die [**Funktion InitializeSecurityContext (Digest),**](initializesecuritycontext--digest.md) um den Prozess zum Einrichten eines Sicherheitskontexts zu starten. Der Server kann mindestens ein Antworttoken vom Remoteclient anfordern, um die Einrichtung des Sicherheitskontexts abzuschließen.

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

Ein Handle für die Anmeldeinformationen des Servers. Der Server ruft die [**AcquireCredentialsHandle (Digest)-Funktion**](acquirecredentialshandle--digest.md) auf, wobei entweder das \_ SECPKG CRED \_ INBOUND- oder SECPKG \_ CRED \_ BOTH-Flag festgelegt ist, um dieses Handle abzurufen.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Digest)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen ist *phContext* das Handle für den teilweise gebildeten Kontext, der im *phNewContext-Parameter* durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) generiert wird, der den Eingabepufferdeskriptor enthält.

Die folgende Tabelle zeigt die Pufferkonfiguration für Digest-HTTP. Der erste Puffer muss vom Typ **SECBUFFER \_ TOKEN** sein, und der Rest muss vom Typ **SECBUFFER \_ PKG \_ PARAMS** sein. SASL erfordert nur Puffer 0 (null).



| Puffertyp \# /buffer                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt> **SECBUFFER-TOKEN \_**</dt> </dl>                                        | Leer für den ersten Aufruf und die Vom Client empfangene Abfrageantwort für den zweiten Aufruf.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Methode. Zeichen sind das Wirelineformat aus der Anforderungszeile. US ASCII-Einzel bytezeichen.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Reserviert.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | HEntity. Hexadezimale Darstellung von H(entity-body). US ASCII-Einzel bytezeichen.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Reich. Bereichszeichenfolge für die Herausforderung. Unicode-Zeichenfolge, die in US ASCII darstellbar sein muss.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt> **SECBUFFER-KANALBINDUNGEN \_ \_** \| **SECBUFFER \_ READONLY**</dt> </dl> | Enthält den Wert des Kanalbindungstokens.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |



 

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mit bitweisen **OR-Vorgängen** kombiniert werden. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> </dl>                                                  | Der Digest ordnet Ausgabepuffer für Sie zu. Wenn Sie die Verwendung der Ausgabepuffer abgeschlossen haben, können Sie sie freigeben, indem Sie die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen.<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ REQ \_ ALLOW \_ MISSING \_ BINDINGS**</dt> </dl>                            | Gibt an, dass Digest keine Kanalbindungen für innere und äußere Kanäle erfordert. Dieser Wert wird aus Gründen der Abwärtskompatibilität verwendet, wenn die Unterstützung für die Endpunktkanalbindung nicht bekannt ist.<br/> Dieser Wert schließen sich mit **ASC \_ REQ PROXY BINDINGS gegenseitig \_ \_ aus.**<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ REQ \_ CONFIDENTIALITY**</dt> </dl>                                                   | Verschlüsseln und Entschlüsseln von Nachrichten. <br/> Der Digest-SSP unterstützt dieses Flag nur für SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**\_ \_ ASC-REQ-PROXYBINDUNGEN \_**</dt> </dl>                                                     | Gibt an, dass digest kanalbindung erfordert.<br/> Dieser Wert schließen sich mit **ASC \_ REQ ALLOW MISSING BINDINGS gegenseitig \_ \_ \_ aus.**<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ REQ \_ CONNECTION**</dt> </dl>                                                                  | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ REQ \_ EXTENDED \_ ERROR**</dt> </dl>                                                     | Wenn Fehler auftreten, wird die Remotepartei benachrichtigt.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ REQ \_ HTTP (0x10000000)**</dt> </dl> | Verwenden Sie Digest für HTTP. Lassen Sie dieses Flag aus, um Digest als SASL-Mechanismus zu verwenden.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ REQ \_ INTEGRITY**</dt> </dl>                                                                     | Signieren von Nachrichten und Überprüfen von Signaturen.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>                                                        | Erkennen wiedergegebener Pakete.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl>                                                  | Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Mögliche Attributflags und ihre Bedeutungen finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC \_ REQ, z. B. ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

Dieser Parameter wird nicht mit Digest-SSP verwendet. Wenn Sie Digest-SSP verwenden, geben Sie 0 (null) für diesen Parameter an.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Digest)** empfängt dieser Zeiger das neue Kontexthandle. Bei nachfolgenden Aufrufen kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)an den Client gesendet. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E OK zurückgibt. \_ Alle generierten Puffer müssen an die Clientanwendung zurückgesendet werden.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC \_ RET, z. B. ASC \_ RET \_ DELEGATE.

Suchen Sie erst nach sicherheitsrelevanten Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. B. das \_ ASC RET \_ ALLOCATED \_ MEMORY-Flag, können vor der endgültigen Rückgabe überprüft werden.

</dd> <dt>

*ptsTimeStamp* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, [*dass das Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurück gibt.

Dieser Parameter wird auf eine konstante maximale Zeit festgelegt. Es gibt keine Ablaufzeit für [*Digestsicherheitskontexte*](../secgloss/s-gly.md)oder Anmeldeinformationen oder bei Verwendung des Digest-SSP.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Fehler bei der Funktion. Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Fehler bei der Anmeldung.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Fehler bei der Funktion. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann folgende Bedingungen haben:<br/><ul><li>Der Domänenname der authentifizierenden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Fehler bei der Funktion. Das im <em>phCredential-Parameter angegebene Anmeldeinformationshandl</em> ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der [*vom Client*](../secgloss/s-gly.md) empfangene Sicherheitskontext wurde akzeptiert. Wenn ein Ausgabetoken von der Funktion generiert wurde, muss es an den Clientprozess gesendet werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>Fehler bei der Funktion. Im fContextReq-Parameter wurde ein ungültiges <em>Kontextattributflag</em> angegeben.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und das Ausgabetoken an den Client übergeben. Der Server wartet dann auf ein Rückgabetoken vom Client und führt dann einen weiteren Aufruf von [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Nachricht vom Client fertigstellen und dann die Funktion [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in <em>pInput für einen</em> weiteren Aufruf von [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md) übergeben werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Fehler bei der Funktion. Die<strong>[AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md)-Funktion wurde aufgerufen, nachdem der angegebene Kontext eingerichtet wurde.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>Fehler bei der Funktion. Die Kanalbindungsrichtlinie wurde nicht erfüllt.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Hinweise

Die **AcceptSecurityContext-Funktion (Digest)** ist das Server-Gegenstück zur [**InitializeSecurityContext-Funktion (Digest).**](initializesecuritycontext--digest.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *Parameter fContextReq,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients [](../secgloss/i-gly.md)in der Lage sein müssen, eine vertrauliche oder integritätsgeprüfte Sitzung zu verwenden, und Clients ablehnen, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts benötigen, und alles, was der Client bereitstellen oder erfordert, wird im *parameter pfContextAttr zurückgegeben.*

Für ein Paket, das mehrseitige Authentifizierung unterstützt, z. B. gegenseitige Authentifizierung, lautet die aufrufende Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server ruft **AcceptSecurityContext (Digest)** zum ersten Mal auf, wodurch ein Antworttoken generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Wenn **InitializeSecurityContext (Digest)** SEC E OK zurückgibt, wurde die gegenseitige Authentifizierung \_ \_ abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Digest) einen** Fehlercode zurückgibt, wird die gegenseitige Authentifizierungsaushandlung beendet. Andernfalls wird das von **InitializeSecurityContext (Digest)** zurückgegebene Sicherheitstoken an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die *Parameter fContextReq* und *pfContextAttr* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

> [!Note]  
> Der *parameter pfContextAttr* ist bei jeder erfolgreichen Rückgabe gültig, aber nur bei der endgültigen erfolgreichen Rückgabe sollten Sie die Flags im Zusammenhang mit Sicherheitsaspekten des Kontexts untersuchen. Zwischenrück rückgaben können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn beispielsweise Vertraulichkeit (Verschlüsselung) angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort herunterfahren. Wenn der [*Sicherheitskontext nicht*](../secgloss/s-gly.md) eingerichtet werden kann, muss der Server den teilweise erstellten Kontext durch Aufrufen der [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) frei geben. Informationen dazu, wann die **DeleteSecurityContext-Funktion aufgerufen werden** soll, finden Sie unter **DeleteSecurityContext**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Clientzertifikat zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Benutzers zu ändern.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
