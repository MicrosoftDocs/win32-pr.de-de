---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen Sicherheitskontext zwischen dem Server und einem Remoteclient herzustellen, der Negotiate verwendet. [](../secgloss/s-gly.md)
ms.assetid: aaec6fee-df6b-4033-8ece-73ecd1799653
title: AcceptSecurityContext(Negotiate)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9ac466530be0a19a6b8c88355f238a1cd491f9c2ff6d7d8dbe67b16ba20f43b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141632"
---
# <a name="acceptsecuritycontext-negotiate-function"></a>AcceptSecurityContext(Negotiate)-Funktion

Mit **der AcceptSecurityContext-Funktion (Negotiate)** kann die Serverkomponente [](../secgloss/s-gly.md) einer Transportanwendung einen Sicherheitskontext zwischen dem Server und einem Remoteclient einrichten. Der Remoteclient verwendet die [**InitializeSecurityContext (Negotiate)-Funktion,**](initializesecuritycontext--negotiate.md) um den Prozess zum Einrichten eines [*Sicherheitskontexts zu starten.*](../secgloss/s-gly.md) Der Server kann mindestens ein Antworttoken vom Remoteclient benötigen, um die Einrichtung des [*Sicherheitskontexts abschließen zu können.*](../secgloss/s-gly.md)

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

Ein Handle für die Anmeldeinformationen des Servers. Der Server ruft die [**AcquireCredentialsHandle (Negotiate)-Funktion**](acquirecredentialshandle--negotiate.md) auf, bei der entweder das SECPKG \_ CRED \_ INBOUND- oder SECPKG CRED BOTH-Flag festgelegt ist, um dieses Handle \_ \_ abzurufen.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Negotiate)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen *ist phContext* das Handle für den teilweise gebildeten Kontext, der vom ersten Aufruf im *phNewContext-Parameter* zurückgegeben wurde.

</dd> <dt>

*pInput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) generiert wird, der den Eingabepufferdeskriptor enthält.

Kanalbindungsinformationen können durch Übergeben einer [**SecBuffer-Struktur**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ **SECBUFFER \_ CHANNEL \_ BINDINGS** zusätzlich zu den Puffern angegeben werden, die durch den Aufruf der [**InitializeSecurityContext (General)-Funktion generiert**](initializesecuritycontext--general.md) werden. Die Kanalbindungsinformationen für den Kanalbindungspuffer können durch Aufrufen der [**QueryContextAttributes-Funktion (Schannel)**](querycontextattributes--schannel.md) im Schannel-Kontext abgerufen werden, den der Client zur Authentifizierung verwendet.

</dd> <dt>

*fContextReq* \[ In\]
</dt> <dd>

Bitflags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mithilfe bitweiser **OR-Vorgänge kombiniert** werden. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ \_ REQ-VERTRAULICHKEIT**</dt> </dl>  | Verschlüsseln und Entschlüsseln von Nachrichten.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ \_ REQ-VERBINDUNG**</dt> </dl>                 | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungsmeldungen.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**\_ASC-REQ-DELEGAT \_**</dt> </dl>                       | Der Server darf die Identität des Clients imitieren. Gültig für Kerberos. Ignorieren Sie dieses Flag für [*die eingeschränkte Delegierung.*](../secgloss/c-gly.md)<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERWEITERTER ASC \_ \_ \_ REQ-FEHLER**</dt> </dl>    | Wenn Fehler auftreten, wird die Remote-Partei benachrichtigt.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ \_ REQ-INTEGRITÄT**</dt> </dl>                    | Signieren von Nachrichten und Überprüfen von Signaturen.<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Erkennen von wiedergegebenen Paketen.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Erkennen von Nachrichten, die nicht sequenziert empfangen werden.<br/>                                                                                                                                                                       |



 

Mögliche Attributflags und deren Bedeutung finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC REQ, z. B. \_ ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *parameter pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ In\]
</dt> <dd>

Die Datendarstellung, z. B. die Byte reihenfolge, auf dem Ziel. Dieser Parameter kann entweder SECURITY \_ NATIVE \_ DREP oder SECURITY \_ NETWORK \_ DREP sein.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (Negotiate)** empfängt dieser Zeiger das neue Kontexthand handle. Bei nachfolgenden Aufrufen *kann phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (Negotiate) an den Client gesendet.**](initializesecuritycontext--negotiate.md) Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E \_ OK zurückgibt. Alle generierten Puffer müssen zurück an die Clientanwendung gesendet werden.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC RET, z. \_ B. ASC \_ RET \_ DELEGATE.

Überprüfen Sie erst nach sicherheitsbezogenen Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wird. Attributflags, die sich nicht auf die Sicherheit bezieht, z. B. das ASC \_ RET ALLOCATED MEMORY-Flag, können vor der \_ \_ endgültigen Rückgabe überprüft werden.

</dd> <dt>

*ptsTimeStamp* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, [*dass das Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in Ortszeit zurück gibt.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>Beschreibung</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Fehler bei der Funktion. Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Fehler bei der Anmeldung.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Fehler bei der Funktion. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann folgende Bedingungen haben:<br/><ul><li>Der Domänenname der authentifizierenden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der [*vom Client*](../secgloss/s-gly.md) empfangene Sicherheitskontext wurde akzeptiert. Wenn ein Ausgabetoken von der Funktion generiert wurde, muss es an den Clientprozess gesendet werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen und das Ausgabetoken an den Client übergeben. Der Server wartet dann auf ein Rückgabetoken vom Client und führt dann einen weiteren Aufruf von [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md) aus.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Erstellung der Nachricht vom Client abschließen und dann die Funktion<strong>[CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufrufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in <em>pInput</em> für einen weiteren Aufruf von [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md) übergeben werden.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Hinweise

Die **AcceptSecurityContext (Negotiate)-Funktion** ist die Serverentsprechung zur [**InitializeSecurityContext (Negotiate)-Funktion.**](initializesecuritycontext--negotiate.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *fContextReq-Parameter,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients [](../secgloss/i-gly.md)eine vertrauliche oder integritätsüberprüfungsbasierte Sitzung verwenden müssen, und Clients ablehnen können, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts erfordern, und das, was der Client bereitstellen kann oder erfordert, wird im *pfContextAttr-Parameter* zurückgegeben.

Für ein Paket, das die mehrstufige Authentifizierung unterstützt, z. B. gegenseitige Authentifizierung, sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server ruft **AcceptSecurityContext (Negotiate)** zum ersten Mal auf, wodurch ein Antworttoken generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Wenn **InitializeSecurityContext (Negotiate)** SEC E OK zurückgibt, wurde die \_ gegenseitige \_ Authentifizierung abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Negotiate)** einen Fehlercode zurückgibt, wird die gegenseitige Authentifizierungsaushandlung beendet. Andernfalls wird das von **InitializeSecurityContext (Negotiate)** zurückgegebene Sicherheitstoken an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die Parameter *fContextReq* und *pfContextAttr* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

> [!Note]  
> Der *pfContextAttr-Parameter* ist bei jeder erfolgreichen Rückgabe gültig, jedoch nur bei der endgültigen erfolgreichen Rückgabe, wenn Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts untersuchen. Zwischenrücksetzungen können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichen. Wenn z. B. Vertraulichkeit (Verschlüsselung) angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext freigeben, indem er die [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) aufruft. Informationen dazu, wann die **DeleteSecurityContext-Funktion** aufgerufen werden soll, finden Sie unter **DeleteSecurityContext**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Clientzertifikat zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Benutzers zu annehmen.

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

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> </dl>

 

 
