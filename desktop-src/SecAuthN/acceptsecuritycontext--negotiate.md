---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einzurichten, der Negotiate verwendet.
ms.assetid: aaec6fee-df6b-4033-8ece-73ecd1799653
title: AcceptSecurityContext(Negotiate)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13aa91545e5301e10a1f9d36e93e2d4995c15253
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628692"
---
# <a name="acceptsecuritycontext-negotiate-function"></a>AcceptSecurityContext (Negotiate)-Funktion

Mit der **Funktion AcceptSecurityContext (Negotiate)** kann die Serverkomponente einer Transportanwendung einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remoteclient einrichten. Der Remoteclient verwendet die [**InitializeSecurityContext (Negotiate)-Funktion,**](initializesecuritycontext--negotiate.md) um den Prozess zum Einrichten eines [*Sicherheitskontexts*](../secgloss/s-gly.md)zu starten. Der Server kann mindestens ein Antworttoken vom Remoteclient anfordern, um die Einrichtung des [*Sicherheitskontexts*](../secgloss/s-gly.md)abzuschließen.

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

Ein Handle für die Anmeldeinformationen des Servers. Der Server ruft die [**AcquireCredentialsHandle (Negotiate)-Funktion**](acquirecredentialshandle--negotiate.md) auf, wobei entweder das SECPKG \_ CRED \_ INBOUND- oder SECPKG \_ CRED \_ BOTH-Flag festgelegt ist, um dieses Handle abzurufen.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Negotiate)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen ist *phContext* das Handle für den teilweise gebildeten Kontext, der im *phNewContext-Parameter* durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) generiert wird, der den Eingabepufferdeskriptor enthält.

Kanalbindungsinformationen können durch Übergeben einer [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ **SECBUFFER \_ CHANNEL \_ BINDINGS** zusätzlich zu den Puffern angegeben werden, die durch den Aufruf der [**InitializeSecurityContext (General)-Funktion**](initializesecuritycontext--general.md) generiert werden. Die Kanalbindungsinformationen für den Kanalbindungspuffer können abgerufen werden, indem die [**QueryContextAttributes (Schannel)-Funktion**](querycontextattributes--schannel.md) für den Schannelkontext aufgerufen wird, den der Client für die Authentifizierung verwendet hat.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mit bitweisen **OR-Vorgängen** kombiniert werden. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ REQ \_ CONFIDENTIALITY**</dt> </dl>  | Verschlüsseln und Entschlüsseln von Nachrichten.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ REQ \_ CONNECTION**</dt> </dl>                 | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ REQ \_ DELEGATE**</dt> </dl>                       | Der Server darf die Identität des Clients annehmen. Gültig für Kerberos. Ignorieren Sie dieses Flag für [*die eingeschränkte Delegierung.*](../secgloss/c-gly.md)<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ REQ \_ EXTENDED \_ ERROR**</dt> </dl>    | Wenn Fehler auftreten, wird die Remotepartei benachrichtigt.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ REQ \_ INTEGRITY**</dt> </dl>                    | Signieren von Nachrichten und Überprüfen von Signaturen.<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Erkennen wiedergegebener Pakete.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Erkennen von Nachrichten, die außerhalb der Sequenz empfangen wurden.<br/>                                                                                                                                                                       |



 

Mögliche Attributflags und ihre Bedeutungen finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC \_ REQ, z. B. ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *pfContextAttr-Parameter.*

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Bytereihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Negotiate)** empfängt dieser Zeiger das neue Kontexthandle. Bei nachfolgenden Aufrufen kann *phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)an den Client gesendet. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E OK zurückgibt. \_ Alle generierten Puffer müssen an die Clientanwendung zurückgesendet werden.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC \_ RET, z. B. ASC \_ RET \_ DELEGATE.

Suchen Sie erst nach sicherheitsrelevanten Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. B. das \_ ASC RET \_ ALLOCATED \_ MEMORY-Flag, können vor der endgültigen Rückgabe überprüft werden.

</dd> <dt>

*ptsTimeStamp* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurückgibt.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Fehler bei der Funktion. Fehler, der keinem SSPI-Fehlercode zugeordnet wurde.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Fehler bei der Anmeldung.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Fehler bei der Funktion. Für die Authentifizierung konnte keine Autorität kontaktiert werden. Dies kann auf die folgenden Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänenname der authentifizierenden Seite ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Fehler bei der Vertrauensstellung.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene [*Sicherheitskontext*](../secgloss/s-gly.md) wurde akzeptiert. Wenn ein Ausgabetoken von der Funktion generiert wurde, muss es an den Clientprozess gesendet werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und das Ausgabetoken an den Client übergeben. Der Server wartet dann auf ein Rückgabetoken vom Client und führt dann einen weiteren Aufruf von [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md) aus.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Nachricht vom Client fertigstellen und dann die Funktion [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in <em>pInput für einen</em> weiteren Aufruf von [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md) übergeben werden.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Hinweise

Die **AcceptSecurityContext(Negotiate)-Funktion** ist das Serverent pendant zur [**InitializeSecurityContext (Negotiate)-Funktion.**](initializesecuritycontext--negotiate.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *Parameter fContextReq,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients [](../secgloss/i-gly.md)in der Lage sein müssen, eine vertrauliche oder integritätsgeprüfte Sitzung zu verwenden, und Clients ablehnen, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts benötigen, und alles, was der Client bereitstellen oder erfordert, wird im *parameter pfContextAttr zurückgegeben.*

Für ein Paket, das mehrseitige Authentifizierung unterstützt, z. B. gegenseitige Authentifizierung, lautet die aufrufende Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server ruft **AcceptSecurityContext (Negotiate)** zum ersten Mal auf, wodurch ein Antworttoken generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Wenn **InitializeSecurityContext (Negotiate)** SEC E OK zurückgibt, wurde die gegenseitige Authentifizierung \_ \_ abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Negotiate) einen** Fehlercode zurückgibt, wird die gegenseitige Authentifizierungsaushandlung beendet. Andernfalls wird das von **InitializeSecurityContext (Negotiate)** zurückgegebene Sicherheitstoken an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

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

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> </dl>

 

 
