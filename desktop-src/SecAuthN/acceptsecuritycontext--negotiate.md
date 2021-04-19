---
description: Ermöglicht der Serverkomponente einer Transport Anwendung das Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) zwischen dem Server und einem Remote Client, der "aushandeln" verwendet.
ms.assetid: aaec6fee-df6b-4033-8ece-73ecd1799653
title: Akzeptsecuritycontext (aushandeln)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d4a9d38618760a97e9475e8d5914d6e54c5eea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362282"
---
# <a name="acceptsecuritycontext-negotiate-function"></a>Akzeptsecuritycontext (aushandeln)-Funktion

Die Funktion " **Accept-SecurityContext (aushandeln)** " ermöglicht der Serverkomponente einer Transport Anwendung das Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) zwischen dem Server und einem Remote Client. Der Remote Client verwendet die [**InitializeSecurityContext (Aushandlungs)**](initializesecuritycontext--negotiate.md) -Funktion, um den Prozess der Einrichtung eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)zu starten. Der Server kann mindestens ein Antwort Token vom Remote Client anfordern, um das Einrichten des [*Sicherheits Kontexts*](../secgloss/s-gly.md)abzuschließen.

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

*phcredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmelde Informationen des Servers. Der Server Ruft die [**AcquireCredentialsHandle (Aushandlungs)**](acquirecredentialshandle--negotiate.md) -Funktion auf, wobei entweder die "secpkg" \_ - \_ oder "secpkg" \_ -Funktion für das \_ Abrufen dieses Handles festgelegt ist.

</dd> <dt>

*phcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten **calltsecuritycontext (aushandeln)** ist dieser Zeiger **null**. Bei nachfolgenden Aufrufen ist *phcontext* das Handle für den teilweise formatierten Kontext, der im *phnewcontext* -Parameter durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pinput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die durch einen Client-aufrufen von [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md) generiert wird, der den Eingabepuffer Deskriptor enthält.

Kanal Bindungs Informationen können angegeben werden, indem eine [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur vom Typ **secbuffer \_ Channel- \_ Bindungen** zusätzlich zu den Puffern übergeben wird, die durch den-Befehl der [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) -Funktion generiert werden. Die channelbindungs Informationen für den channelbindungs Puffer können durch Aufrufen der [**QueryContextAttributes-Funktion (SChannel)**](querycontextattributes--schannel.md) im SChannel-Kontext abgerufen werden, den der Client für die Authentifizierung verwendet hat.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Bitflags, die die Attribute angeben, die vom Server zum Einrichten des Kontexts benötigt werden. Bitflags können mithilfe von bitweisen **or** -Vorgängen kombiniert werden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ req- \_ Vertraulichkeit**</dt> </dl>  | Verschlüsseln und Entschlüsseln von Nachrichten.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ req- \_ Verbindung**</dt> </dl>                 | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungs Meldungen.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ req-Delegat \_**</dt> </dl>                       | Der Server kann die Identität des Clients annehmen. Gültig für Kerberos. Dieses Flag für die [*eingeschränkte Delegierung*](../secgloss/c-gly.md)ignorieren.<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_Erweiterte ASC req- \_ \_ Fehler**</dt> </dl>    | Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ req- \_ Integrität**</dt> </dl>                    | Signieren von Nachrichten und Überprüfen von Signaturen<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ req \_ Replay \_ Detect**</dt> </dl>       | Erkennen wieder gewiedergabe Pakete.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ req- \_ Sequenz \_ Erkennung**</dt> </dl> | Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/>                                                                                                                                                                       |



 

Informationen zu möglichen Attributflags und deren Bedeutung finden Sie unter [Kontext Anforderungen](context-requirements.md). Flags, die für diesen Parameter verwendet werden, wird ASC \_ req vorangestellt, z \_ . b. asc req-Delegat \_ .

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Die Datendarstellung (z. b. Byte Reihenfolge) für das Ziel. Dieser Parameter kann entweder "Security \_ native \_ drep" oder "Security \_ Network \_ drep" lauten.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten **calltsecuritycontext (aushandeln)**-Befehl empfängt dieser Zeiger das neue Kontext handle. Bei nachfolgenden Aufrufen kann *phnewcontext* mit dem im Parameter *phcontext* angegebenen Handle identisch sein.

</dd> <dt>

*poutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die den Ausgabepuffer Deskriptor enthält. Dieser Puffer wird an den Client gesendet, damit er in weitere Aufrufe von [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md)eingegeben werden kann. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion sec \_ E OK zurückgibt \_ . Jeder generierte Puffer muss an die Client Anwendung zurückgesendet werden.

</dd> <dt>

*pfContextAttr* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Die für diesen Parameter verwendeten Flags haben das Präfix ASC \_ RET, z. b. asc ret-Delegat \_ \_ .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag, können vor der letzten Rückgabe geprüft werden

</dd> <dt>

*ptstimestamp* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in der Ortszeit zurückgibt.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungs Vorgangs kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung Weitere Informationen bereitgestellt werden. Daher muss *ptstimestamp* bis zum letzten aufrufsbefehl **null** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion über gegebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion übergebenen Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030cl</dt> </dl></td><td>Die Anmeldung ist fehlgeschlagen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann auf folgende Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänen Name der authentifizier enden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene [*Sicherheitskontext*](../secgloss/s-gly.md) wurde akzeptiert. Wenn ein Ausgabe Token von der-Funktion generiert wurde, muss es an den Client Prozess gesendet werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen und das Ausgabe Token an den Client übergeben. Der Server wartet dann auf ein Rückgabe Token vom Client und führt dann einen weiteren [<strong>Accept tsecuritycontext (Aushandlungs)</strong>] (AcceptSecurityContext--Negotiate.MD)-Befehl aus.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Meldung vom Client abschließen und dann die Funktion [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabe Token an den Client senden und auf ein zurück gegebenes Token warten. Das zurückgegebene Token sollte in <em>pinput</em> für einen weiteren [accept-<strong>SecurityContext (Aushandlungs)</strong>] (AcceptSecurityContext--Negotiate.MD)-Befehl übergebenen werden.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Bemerkungen

Die **akzeptsecuritycontext (Aushandlungs)** -Funktion ist der Server, der der [**InitializeSecurityContext (Aushandlungs)**](initializesecuritycontext--negotiate.md) -Funktion entspricht.

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *fContextReq* -Parameter, um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients in der Lage sein müssen, eine vertrauliche Sitzung oder eine [*Integritäts*](../secgloss/i-gly.md)aktivierte Sitzung zu verwenden, und Clients ablehnen können, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts erfordern, und das, was der Client bereitstellen oder erfordert, wird im Parameter " *pfContextAttr* " zurückgegeben.

Für ein Paket, das die Authentifizierung mit mehreren Seiten unterstützt, wie z. b. die gegenseitige Authentifizierung, lautet die Aufruf Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server Ruft beim ersten Mal " **akzeptsecuritycontext (aushandeln)** " auf, wodurch ein Antwort Token generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md). Wenn **InitializeSecurityContext (aushandeln)** sec E OK zurückgibt, wurde die \_ \_ gegenseitige Authentifizierung abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (aushandeln)** einen Fehlercode zurückgibt, endet die Aushandlung der gegenseitigen Authentifizierung. Andernfalls wird das von **InitializeSecurityContext (aushandeln)** zurückgegebene Sicherheits Token an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die Parameter " *f* " und " *pfContextAttr* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

> [!Note]  
> Der *pfContextAttr* -Parameter ist bei erfolgreicher Rückgabe gültig, aber nur bei der letzten erfolgreichen Rückgabe sollten Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts untersuchen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit (Verschlüsselung) angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben. Informationen dazu, wann Sie die **Delta Context** -Funktion aufzurufen, finden Sie unter **Delta Context**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**querysecuritycontexttoken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) -Funktion verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Client Zertifikat zugeordnet wurde. Der Server kann die Identität des Benutzers auch mit der Identität [**atesecuritycontext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) -Funktion annehmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Delta Context-Kontext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md)
</dt> </dl>

 

 
