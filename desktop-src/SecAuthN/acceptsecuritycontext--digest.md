---
description: Ermöglicht der Serverkomponente einer Transport Anwendung das Einrichten eines Sicherheits Kontexts zwischen dem Server und einem Remote Client, der Digest verwendet.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: Akzeptsecuritycontext (Digest)-Funktion (SSPI. h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 11ffa801612f14f5b9aaf61e7d48b61377bc9e56
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050734"
---
# <a name="acceptsecuritycontext-digest-function"></a>Akzeptsecuritycontext (Digest)-Funktion

Die Funktion " **Accept-SecurityContext (Digest)** " ermöglicht der Serverkomponente einer Transport Anwendung, einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen dem Server und einem Remote Client einzurichten. Der Remote Client verwendet die [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) -Funktion, um den Prozess der Einrichtung eines Sicherheits Kontexts zu starten. Der Server kann mindestens ein Antwort Token vom Remote Client anfordern, um das Einrichten des Sicherheits Kontexts abzuschließen.

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

*phcredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmelde Informationen des Servers. Der Server Ruft die Funktion " [**AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md) " auf, wobei entweder die "secpkg" \_ - \_ oder "secpkg" \_ -Funktion für das \_ Abrufen dieses Handles festgelegt ist.

</dd> <dt>

*phcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufe von " **Accept-SecurityContext" (Digest)** ist dieser Zeiger **null**. Bei nachfolgenden Aufrufen ist *phcontext* das Handle für den teilweise formatierten Kontext, der im *phnewcontext* -Parameter durch den ersten Aufruf zurückgegeben wurde.

</dd> <dt>

*pinput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die durch einen Client-aufrufen von [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) generiert wird, der den Eingabepuffer Deskriptor enthält.

In der folgenden Tabelle wird die Puffer Konfiguration für Digest http angezeigt. Der erste Puffer muss den Typ ' **secbuffer \_ Token**' aufweisen, und der Rest muss den Typ ' **secbuffer \_ pkg \_**' aufweisen. SASL erfordert nur Puffer NULL.



| Buffer \# /buffer Type                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt> **secbuffer- \_ Token**</dt> </dl>                                        | Leer für den ersten-Befehl und die Challenge-Antwort, die vom Client für den zweiten-Befehl empfangen wird.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **secbuffer \_ pkg \_** -Parameter</dt> </dl>                                  | Methode. Zeichen sind das Wireline-Format aus der Anforderungs Zeile. US-ASCII-Einzel Byte Zeichen.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **secbuffer \_ pkg \_** -Parameter</dt> </dl>                                  | Reserviert.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt> **secbuffer \_ pkg \_** -Parameter</dt> </dl>                                  | Hentity. Hexadezimale Darstellung von H (entitätentext). US-ASCII-Einzel Byte Zeichen.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **secbuffer \_ pkg \_** -Parameter</dt> </dl>                                  | Realm. Bereichs Zeichenfolge für die Herausforderung. Unicode-Zeichenfolge, die in US-ASCII darstellbar sein muss.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt> **secbuffer- \_ Kanal \_ Bindungen** \| **secbuffer \_** schreibgeschützt</dt> </dl> | Enthält den Wert für das channelbindungstoken.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> |



 

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Bitflags, die die Attribute angeben, die vom Server zum Einrichten des Kontexts benötigt werden. Bitflags können mithilfe von bitweisen **or** -Vorgängen kombiniert werden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ req \_ Arbeits \_ Speicher zuweisen**</dt> </dl>                                                  | Digest ordnet Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufrufen.<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ req \_ lässt \_ fehlende \_ Bindungen zu.**</dt> </dl>                            | Gibt an, dass der Digest keine Kanal Bindungen für innere und äußere Kanäle erfordert. Dieser Wert wird aus Gründen der Abwärtskompatibilität verwendet, wenn die Unterstützung für die Endpunkt kanalbindung nicht bekannt ist.<br/> Dieser Wert schließt sich mit **ASC \_ req- \_ Proxy \_ Bindungen** gegenseitig aus.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**ASC \_ req- \_ Vertraulichkeit**</dt> </dl>                                                   | Verschlüsseln und Entschlüsseln von Nachrichten. <br/> Der Digest-SSP unterstützt dieses Flag nur für SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**ASC \_ req- \_ Proxy \_ Bindungen**</dt> </dl>                                                     | Gibt an, dass der Digest eine channelbindung erfordert.<br/> Dieser Wert schließt sich gegenseitig aus, wenn **ASC \_ req \_ \_ fehlende \_ Bindungen zulässt**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**ASC \_ req- \_ Verbindung**</dt> </dl>                                                                  | Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungs Meldungen.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_Erweiterte ASC req- \_ \_ Fehler**</dt> </dl>                                                     | Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ req \_ http (0x10000000)**</dt> </dl> | Verwenden Sie Digest für http. Lassen Sie dieses Flag aus, um Digest als SASL-Mechanismus zu verwenden.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**ASC \_ req- \_ Integrität**</dt> </dl>                                                                     | Signieren von Nachrichten und Überprüfen von Signaturen<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ req \_ Replay \_ Detect**</dt> </dl>                                                        | Erkennen wieder gewiedergabe Pakete.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ req- \_ Sequenz \_ Erkennung**</dt> </dl>                                                  | Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Informationen zu möglichen Attributflags und deren Bedeutung finden Sie unter [Kontext Anforderungen](context-requirements.md). Flags, die für diesen Parameter verwendet werden, wird ASC \_ req vorangestellt, z \_ . b. asc req-Delegat \_ .

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Die Datendarstellung (z. b. Byte Reihenfolge) für das Ziel. Dieser Parameter kann entweder "Security \_ native \_ drep" oder "Security \_ Network \_ drep" lauten.

Dieser Parameter wird nicht mit Digest-SSP verwendet. Wenn Sie Digest-SSP verwenden, geben Sie 0 für diesen Parameter an.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten **calltsecuritycontext (Digest)**-Befehl empfängt dieser Zeiger das neue Kontext handle. Bei nachfolgenden Aufrufen kann *phnewcontext* mit dem im Parameter *phcontext* angegebenen Handle identisch sein.

</dd> <dt>

*poutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die den Ausgabepuffer Deskriptor enthält. Dieser Puffer wird an den Client gesendet, damit er in weitere Aufrufe von [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)eingegeben werden kann. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion sec \_ E OK zurückgibt \_ . Jeder generierte Puffer muss an die Client Anwendung zurückgesendet werden.

</dd> <dt>

*pfContextAttr* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfängt, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Die für diesen Parameter verwendeten Flags haben das Präfix ASC \_ RET, z. b. asc ret-Delegat \_ \_ .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag, können vor der letzten Rückgabe geprüft werden

</dd> <dt>

*ptstimestamp* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in der Ortszeit zurückgibt.

Dieser Parameter ist auf eine Konstante maximale Zeit festgelegt. Es gibt keine Ablaufzeit für Digest- [*Sicherheitskontext*](../secgloss/s-gly.md)-oder-Anmelde Informationen oder bei Verwendung des Digest-SSP.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungs Vorgangs kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung Weitere Informationen bereitgestellt werden. Daher muss *ptstimestamp* bis zum letzten aufrufsbefehl **null** sein.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Rückgabecode/-wert</th><th>BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion über gegebene Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Das an die Funktion übergebenen Token ist ungültig.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030cl</dt> </dl></td><td>Die Anmeldung ist fehlgeschlagen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann auf folgende Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänen Name der authentifizier enden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030el</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Der im Parameter " <em>phcredential</em> " angegebene Anmelde Informations Handle ist ungültig.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene [*Sicherheitskontext*](../secgloss/s-gly.md) wurde akzeptiert. Wenn ein Ausgabe Token von der-Funktion generiert wurde, muss es an den Client Prozess gesendet werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Im <em>fContextReq</em> -Parameter wurde ein ungültiges Kontext Attribut Flag angegeben.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen und das Ausgabe Token an den Client übergeben. Der Server wartet dann auf ein Rückgabe Token vom Client und führt dann einen weiteren aufrufungstoken [<strong>Accept tsecuritycontext (Digest)</strong>] (AcceptSecurityContext--Digest.MD) aus.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Meldung vom Client abschließen und dann die Funktion [<strong>completeauthtoken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) aufzurufen.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312l</dt> </dl></td><td>Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabe Token an den Client senden und auf ein zurück gegebenes Token warten. Das zurückgegebene Token sollte in <em>pinput</em> für einen weiteren [accept-<strong>SecurityContext (Digest)</strong>] (AcceptSecurityContext--Digest.MD)-Befehl übergebenen werden.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xc000006dl</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Die [<strong>Accept-SecurityContext (Digest)</strong>] (AcceptSecurityContext--Digest.MD)-Funktion wurde aufgerufen, nachdem der angegebene Kontext festgelegt wurde.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346l</dt> </dl></td><td>Die Funktion ist fehlgeschlagen. Die Kanal Bindungs Richtlinie wurde nicht erfüllt.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Bemerkungen

Die Funktion " **Accept-SecurityContext (Digest)** " ist der Server, der der Funktion " [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) " entspricht.

Wenn der Server eine Anforderung von einem Client empfängt, verwendet der Server den *fContextReq* -Parameter, um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server angeben, dass Clients in der Lage sein müssen, eine vertrauliche Sitzung oder eine [*Integritäts*](../secgloss/i-gly.md)aktivierte Sitzung zu verwenden, und Clients ablehnen können, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts erfordern, und das, was der Client bereitstellen oder erfordert, wird im Parameter " *pfContextAttr* " zurückgegeben.

Für ein Paket, das die Authentifizierung mit mehreren Seiten unterstützt, wie z. b. die gegenseitige Authentifizierung, lautet die Aufruf Sequenz wie folgt:

1.  Der Client überträgt ein Token an den Server.
2.  Der Server Ruft beim ersten Mal ' **akzeptsecuritycontext (Digest)** ' auf, der ein Antwort Token generiert, das dann an den Client gesendet wird.
3.  Der Client empfängt das Token und übergibt es an [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md). Wenn **InitializeSecurityContext (Digest)** sec E OK zurückgibt, wurde die \_ \_ gegenseitige Authentifizierung abgeschlossen, und eine sichere Sitzung kann beginnen. Wenn **InitializeSecurityContext (Digest)** einen Fehlercode zurückgibt, endet die Aushandlung für die gegenseitige Authentifizierung. Andernfalls wird das von **InitializeSecurityContext (Digest)** zurückgegebene Sicherheits Token an den Client gesendet, und die Schritte 2 und 3 werden wiederholt.

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

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
