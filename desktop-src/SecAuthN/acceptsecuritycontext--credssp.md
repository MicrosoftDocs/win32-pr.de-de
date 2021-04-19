---
description: Ermöglicht der Serverkomponente einer Transport Anwendung das Einrichten eines Sicherheits Kontexts zwischen dem Server und einem Remote Client.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Akzeptsecuritycontext (kredssp)-Funktion
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353501"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Akzeptsecuritycontext (kredssp)-Funktion

Mit der Funktion " **Accept-SecurityContext" ("andssp")** kann die Serverkomponente einer Transport Anwendung einen Sicherheitskontext zwischen dem Server und einem Remote Client einrichten. Der Remote Client ruft die [**InitializeSecurityContext (**](initializesecuritycontext--credssp.md) aufgerufenen)-Funktion auf, um den Prozess der Einrichtung eines Sicherheits Kontexts zu starten. Der Server kann mindestens ein Antwort Token vom Remote Client anfordern, um das Einrichten des Sicherheits Kontexts abzuschließen.

## <a name="syntax"></a>Syntax

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parameter

*phcredential* \[ in, optional\]

Ein Handle für die Server Anmelde Informationen. Um dieses Handle abzurufen, ruft der Server die Funktion [**AcquireCredentialsHandle (kredssp)**](acquirecredentialshandle--credssp.md) entweder mit der "secpkg up \_ INBOUND"-oder "secpkg"-Funktion auf, die \_ \_ \_ beide Flags festgelegt sind.

*phcontext* \[ in, optional\]

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufen von " **Accept-SecurityContext" (** aufzurufen) ist dieser Zeiger **null**. Bei nachfolgenden Aufrufen gibt *phcontext* den teilweise formatierten Kontext an, der im *phnewcontext* -Parameter durch den ersten Aufruf zurückgegeben wird.

*pinput* \[ in, optional\]

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die durch einen Client aufrufen von [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md)generiert wird. Die-Struktur enthält den Eingabepuffer Deskriptor.

Der erste Puffer muss den Typ " **secbuffer \_ Token** " aufweisen und das vom Client empfangene Sicherheits Token enthalten. Der zweite Puffer muss den Typ " **secbuffer \_ empty**" aufweisen.

*"f"* \[ in\]

-Bitflags, die die Attribute angeben, die vom Server zum Einrichten des Kontexts benötigt werden. Bitflags können mithilfe von bitweisen **or** -Vorgängen kombiniert werden. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.

| Wert                          | Bedeutung                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ req \_ Arbeits \_ Speicher zuweisen** | Der Credential Security Support Provider (kredssp) weist Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufrufen. |
| **ASC \_ req- \_ Verbindung**       | Der Sicherheitskontext verarbeitet keine Formatierungs Meldungen.                                                                                                                                                      |
| **ASC \_ req-Delegat \_**         | Der Server kann die Identität des Clients annehmen. Dieses Flag für die eingeschränkte Delegierung ignorieren.                                                         |
| **\_Erweiterte ASC req- \_ \_ Fehler**  | Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.                                                                                                                                                          |
| **ASC \_ req \_ Replay \_ Detect**   | Erkennen wieder gewiedergabe Pakete.                                                                                                                                                                                       |
| **ASC \_ req- \_ Sequenz \_ Erkennung** | Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.                                                                                                                                                                      |
| **ASC \_ req- \_ Stream**           | Unterstützen einer Datenstrom orientierten Verbindung.                                                                                                                                                                          |

Informationen zu möglichen Attributflags und deren Bedeutung finden Sie unter [Kontext Anforderungen](context-requirements.md). Flags, die für diesen Parameter verwendet werden, wird ASC \_ req vorangestellt, z \_ . b. asc req-Delegat \_ .

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

*Targetdatarep* \[ in\]

Die Datendarstellung (z. b. Byte Reihenfolge) für das Ziel. Dieser Parameter kann entweder " **Security \_ native \_ drep** " oder " **Security \_ Network \_ drep**" lauten.

*phnewcontext* \[ in, out, optional\]

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufen von " **Accept-SecurityContext" (** aufzurufen) empfängt dieser Zeiger das neue Kontext handle. Bei nachfolgenden Aufrufen kann *phnewcontext* mit dem im Parameter *phcontext* angegebenen Handle identisch sein.

*poutput* \[ in, out, optional\]

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die den Ausgabepuffer Deskriptor enthält. Dieser Puffer wird an den Client gesendet, damit er in weitere Aufrufe von [**InitializeSecurityContext (aufzurufen)**](initializesecuritycontext--credssp.md)eingegeben wird. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion sec \_ E OK zurückgibt \_ . Jeder generierte Puffer muss an die Client Anwendung zurückgesendet werden.

Bei der Ausgabe empfängt dieser Puffer ein Token für den Sicherheitskontext. Das Token muss an den Client gesendet werden. Die Funktion kann auch einen Puffer vom Typ "secbuffer extra" zurückgeben \_ .

*pfContextAttr* \[ vorgenommen\]

Ein Zeiger auf einen Satz von Bitflags, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Die für diesen Parameter verwendeten Flags haben das Präfix ASC \_ RET, z. b. asc ret-Delegat \_ \_ .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag, können vor der letzten Rückgabe geprüft werden

*ptsexpiry* \[ Out, optional\]

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das Sicherheitspaket diesen Wert immer in der Ortszeit zurückgibt.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungs Vorgangs kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung Weitere Informationen bereitgestellt werden. Daher muss *ptstimestamp* bis zum letzten aufrufsbefehl **null** sein.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.

| Rückgabecode/-wert                                   | BESCHREIBUNG                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318l          | Die Funktion wurde erfolgreich ausgeführt. Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss zusätzliche Daten vom Client lesen und " [<strong>akzeptsecuritycontext (</strong>](acceptsecuritycontext--credssp.md) aufzurufen)" erneut aufrufen. |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300l         | Die Funktion ist fehlgeschlagen. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304l              | Die Funktion ist fehlgeschlagen. Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003l              | Die Funktion ist fehlgeschlagen. Das an die Funktion über gegebene Handle ist ungültig.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308l               | Die Funktion ist fehlgeschlagen. Das an die Funktion übergebenen Token ist ungültig.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030cl                | Die Anmeldung ist fehlgeschlagen.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311l | Die Funktion ist fehlgeschlagen. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann auf folgende Bedingungen zurückzuführen sein:<br/><ul><li>Der Domänen Name der authentifizier enden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030el               | Die Funktion ist fehlgeschlagen. Der im Parameter " *phcredential* " angegebene Anmelde Informations Handle ist ungültig.                            |
| SEC_E_OK <br/> 0x00000000L                          | Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene Sicherheitskontext wurde akzeptiert. Wenn die Funktion ein Ausgabe Token generiert hat, muss das Token an den Client Prozess gesendet werden. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302l        | Die Funktion ist fehlgeschlagen. Der *fContextReq* -Parameter hat ein ungültiges Kontext Attribut Flag (ASC_REQ_DELEGATE oder ASC_REQ_PROMPT_FOR_CREDS) angegeben.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314l       | Die Funktion wurde erfolgreich ausgeführt. Der Server muss [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) aufzurufen und das Ausgabe Token an den Client übergeben. Der Server muss dann auf ein Rückgabe Token vom Client warten, bevor er einen weiteren [**calltsecuritycontext (**](acceptsecuritycontext--credssp.md)aufzurufen) aufruft. |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313l             | Die Funktion wurde erfolgreich ausgeführt. Der Server muss die Nachricht vom Client vor dem Aufrufen von [ **completeauthtoken** abschließen.](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312l             | Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabe Token an den Client senden und auf ein zurück gegebenes Token warten. Das zurückgegebene Token sollte bei einem weiteren Aufrufen von "Accept- [**SecurityContext (kredssp)**](acceptsecuritycontext--credssp.md)" in *pinput* übergeben werden.


## <a name="remarks"></a>Bemerkungen

Die Funktion " **Accept-SecurityContext (** Auflistungs Kontext)" ist der Server, der der Funktion " [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md) " entspricht.

Wenn der Server eine Anforderung von einem Client empfängt, verwendet er den *fContextReq* -Parameter, um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server verlangen, dass Clients eine vertrauliche oder [*Integritäts*](../secgloss/i-gly.md)aktivierte Sitzung verwenden können. Clients, die diese Anforderung nicht erfüllen können, können abgelehnt werden. Alternativ kann ein Server nichts erfordern. was der Client erfordert oder bereitstellen kann, wird im Parameter *pfContextAttr* zurückgegeben.

Die Parameter " *f* " und " *pfContextAttr* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

> [!Note]  
> Während der Parameter " *pfContextAttr* " bei erfolgreicher Rückgabe gültig ist, sollten Sie die Flags in Bezug auf Sicherheitsaspekte des Kontexts nur bei der letzten erfolgreichen Rückgabe überprüfen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag.

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit (Verschlüsselung) angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden. Wenn der Sicherheitskontext nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben. Informationen dazu, wann Sie die **Delta Context** -Funktion aufzurufen, finden Sie unter **Delta Context**.

Nachdem der Sicherheitskontext eingerichtet wurde, kann die Serveranwendung die [**querysecuritycontexttoken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) -Funktion verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Client Zertifikat zugeordnet wurde. Der Server kann die Identität des Benutzers auch mit der Identität [**atesecuritycontext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) -Funktion annehmen.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows Vista \[ -Desktop-Apps\]       |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2008 \[ -Desktop-Apps\] |
| Header                   | SSPI. h (Include Security. h)               |
| Bibliothek                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Delta Context-Kontext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md)
