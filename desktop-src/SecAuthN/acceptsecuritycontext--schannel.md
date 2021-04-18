---
description: Ermöglicht der Serverkomponente einer Transport Anwendung das Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) zwischen dem Server und einem Remote Client, der Schannel verwendet.
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: Akzeptsecuritycontext (SChannel)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: ba353cfbe64d6471230a720680301ebab0da511a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359110"
---
# <a name="acceptsecuritycontext-schannel-function"></a>Akzeptsecuritycontext-Funktion (SChannel)

Mit der Funktion " **akzeptsecuritycontext" (SChannel)** kann die Serverkomponente einer Transport Anwendung einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remote Client einrichten. Der Remote Client verwendet die [**InitializeSecurityContext-Funktion (SChannel)**](initializesecuritycontext--schannel.md) , um den Prozess der Einrichtung eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)zu starten. Der Server kann mindestens ein Antwort Token vom Remote Client anfordern, um das Einrichten des [*Sicherheits Kontexts*](../secgloss/s-gly.md)abzuschließen.

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

Ein Handle für die Anmelde Informationen des Servers. Der Server Ruft die Funktion " [**AcquireCredentialsHandle" (SChannel)**](acquirecredentialshandle--schannel.md) mit der "secpkg" \_ - \_ oder "secpkg" \_ -Funktion \_ auf, die für das Abrufen dieses Handles festgelegt ist.

</dd> <dt>

*phcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten **calltsecuritycontext (SChannel)**-Befehl ist dieser Zeiger **null**. Bei nachfolgenden Aufrufen ist *phcontext* das Handle für den teilweise formatierten Kontext, der im *phnewcontext* -Parameter durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pinput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die durch einen Client-aufrufen von [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) generiert wird, der den Eingabepuffer Deskriptor enthält.

Bei Verwendung des SChannel- [*Security Support Provider*](../secgloss/s-gly.md) (SSP) muss der erste Puffer vom Typ "secbuffer \_ Token" sein und das vom Client empfangene Sicherheits Token enthalten. Der zweite Puffer muss den Typ "secbuffer \_ empty" aufweisen.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Bitflags, die die Attribute angeben, die vom Server zum Einrichten des Kontexts benötigt werden. Bitflags können mithilfe von bitweisen **or** -Vorgängen kombiniert werden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ req \_ Arbeits \_ Speicher zuweisen**</dt> </dl> | Digest und SChannel weisen Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufrufen.<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ req- \_ Vertraulichkeit**</dt> </dl>  | Verschlüsseln und Entschlüsseln von Nachrichten.<br/> Der Digest-SSP unterstützt dieses Flag nur für SASL.<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ req- \_ Verbindung**</dt> </dl>                 | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungs Meldungen.<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_Erweiterte ASC req- \_ \_ Fehler**</dt> </dl>    | Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**ASC \_ req- \_ gegenseitige Authentifizierung \_**</dt> </dl>             | Der Client muss ein Zertifikat bereitstellen, das für die Client Authentifizierung verwendet werden kann.<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ req \_ Replay \_ Detect**</dt> </dl>       | Erkennen wieder gewiedergabe Pakete.<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ req- \_ Sequenz \_ Erkennung**</dt> </dl> | Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**ASC \_ req- \_ Stream**</dt> </dl>                             | Unterstützen einer Datenstrom orientierten Verbindung.<br/> Dieses Flag wird nur von SChannel unterstützt.<br/>                                                                                                    |



 

Informationen zu möglichen Attributflags und deren Bedeutung finden Sie unter [Kontext Anforderungen](context-requirements.md). Flags, die für diesen Parameter verwendet werden, wird ASC \_ req vorangestellt, z \_ . b. asc req-Delegat \_ .

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht mit SChannel verwendet. Geben Sie NULL für diesen Parameter an.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten **calltsecuritycontext (SChannel)**-Befehl empfängt dieser Zeiger das neue Kontext handle. Bei nachfolgenden Aufrufen kann *phnewcontext* mit dem im Parameter *phcontext* angegebenen Handle identisch sein.

</dd> <dt>

*poutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die den Ausgabepuffer Deskriptor enthält. Dieser Puffer wird an den Client gesendet, damit er in weitere Aufrufe von [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)eingegeben werden kann. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion sec \_ E OK zurückgibt \_ . Jeder generierte Puffer muss an die Client Anwendung zurückgesendet werden.

Bei der Ausgabe empfängt dieser Puffer ein Token für den [*Sicherheitskontext*](../secgloss/s-gly.md). Das Token muss an den Client gesendet werden. Die Funktion kann auch einen Puffer vom Typ "secbuffer extra" zurückgeben \_ . Außerdem muss der Aufrufer einen Puffer vom Typ " **secbuffer- \_ Warnung**" übergeben. Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Die für diesen Parameter verwendeten Flags haben das Präfix ASC \_ RET, z. b. asc ret-Delegat \_ \_ .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag, können vor der letzten Rückgabe geprüft werden

</dd> <dt>

*ptstimestamp* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in der Ortszeit zurückgibt.

Dies ist bei Verwendung des Schannel-SSP optional. Wenn die Remote Partei ein Zertifikat bereitgestellt hat, das für die Authentifizierung verwendet werden soll, erhält dieser Parameter die Ablaufzeit für dieses Zertifikat. Wenn kein Zertifikat angegeben wurde, wird ein maximaler Zeitwert zurückgegeben.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungs Vorgangs kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung Weitere Informationen bereitgestellt werden. Daher muss *ptstimestamp* bis zum letzten aufrufsbefehl **null** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss zusätzliche Daten vom Client lesen und [<strong>Accept tsecuritycontext (SChannel)</strong>] (AcceptSecurityContext--Schannel.MD) erneut aufzurufen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der <em>pinput</em> -Puffer eine [<strong>secbuffer</strong>] (/Windows/Win32/API/SSPI/NS-SSPI-secbuffer)-Struktur mit einem <strong>buffertype</strong> -Member <strong>SECBUFFER_MISSING</strong>. Der <strong>cbbuffer</strong> -Member von <strong>secbuffer</strong> enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann die Verwendung der-Funktion die Leistung unterstützen, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion über gegebene Handle ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion übergebenen Token ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030cl</dt> </dl></td><td>Die Anmeldung ist fehlgeschlagen.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann auf folgende Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänen Name der authentifizier enden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030el</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Der im Parameter " <em>phcredential</em> " angegebene Anmelde Informations Handle ist ungültig. Dieser Wert kann zurückgegeben werden, wenn der Digest oder Schannel SSP verwendet wird.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene [*Sicherheitskontext*](../secgloss/s-gly.md) wurde akzeptiert. Wenn ein Ausgabe Token von der-Funktion generiert wurde, muss es an den Client Prozess gesendet werden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Im <em>fContextReq</em> -Parameter wurde ein ungültiges kontextattributsflag (ASC_REQ_DELEGATE oder ASC_REQ_PROMPT_FOR_CREDS) angegeben.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367l</dt> </dl></td><td>Zwischen dem Client und dem Server ist kein gängiges Anwendungsprotokoll vorhanden.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen und das Ausgabe Token an den Client übergeben. Der Server wartet dann auf ein Rückgabe Token vom Client und führt dann einen weiteren aufrufungstoken [<strong>Accept tsecuritycontext (SChannel)</strong>] (AcceptSecurityContext--Schannel.MD) aus. <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Meldung vom Client abschließen und dann die Funktion [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabe Token an den Client senden und auf ein zurück gegebenes Token warten. Das zurückgegebene Token sollte in <em>pinput</em> für einen weiteren [accept-<strong>SecurityContext (SChannel)</strong>] (AcceptSecurityContext--Schannel.MD)-Befehl übergebenen werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xc000006dl</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Die [<strong>Accept-SecurityContext (SChannel)</strong>] (AcceptSecurityContext--Schannel.MD)-Funktion wurde aufgerufen, nachdem der angegebene Kontext festgelegt wurde. Dieser Wert kann zurückgegeben werden, wenn der Digest-SSP verwendet wird.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Bemerkungen

Die Funktion " **Accept-SecurityContext" (SChannel)** ist der Server, der der [**InitializeSecurityContext-Funktion (SChannel)**](initializesecuritycontext--schannel.md) entspricht.

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *fContextReq* -Parameter, um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients in der Lage sein müssen, eine vertrauliche Sitzung oder eine [*Integritäts*](../secgloss/i-gly.md)aktivierte Sitzung zu verwenden, und Clients ablehnen können, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts erfordern, und das, was der Client bereitstellen oder erfordert, wird im Parameter " *pfContextAttr* " zurückgegeben.

Für ein Paket, das die Authentifizierung mit mehreren Seiten unterstützt, wie z. b. die gegenseitige Authentifizierung, lautet die Aufruf Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server Ruft beim ersten Mal " **akzeptsecuritycontext (SChannel)** " auf, wodurch ein Antwort Token generiert wird, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md). Wenn **InitializeSecurityContext (SChannel)** sec E OK zurückgibt, wurde die \_ \_ gegenseitige Authentifizierung abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (SChannel)** einen Fehlercode zurückgibt, endet die Aushandlung für die gegenseitige Authentifizierung. Andernfalls wird das von **InitializeSecurityContext (SChannel)** zurückgegebene Sicherheits Token an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

Die Parameter " *f* " und " *pfContextAttr* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

> [!Note]  
> Der *pfContextAttr* -Parameter ist bei erfolgreicher Rückgabe gültig, aber nur bei der letzten erfolgreichen Rückgabe sollten Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts untersuchen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag.

 

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit (Verschlüsselung) angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben. Informationen dazu, wann Sie die **Delta Context** -Funktion aufzurufen, finden Sie unter **Delta Context**.

Nachdem der [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wurde, kann die Serveranwendung die [**querysecuritycontexttoken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) -Funktion verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Client Zertifikat zugeordnet wurde. Der Server kann die Identität des Benutzers auch mit der Identität [**atesecuritycontext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) -Funktion annehmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Delta Context-Kontext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
