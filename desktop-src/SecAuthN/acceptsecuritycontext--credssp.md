---
description: Ermöglicht es der Serverkomponente einer Transportanwendung, einen Sicherheitskontext zwischen dem Server und einem Remoteclient herzustellen.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: AcceptSecurityContext-Funktion (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: df4c87274c3a19d9e4a028cde813801688ce1927d1a0b89dbe3a7e8633ce8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141693"
---
# <a name="acceptsecuritycontext-credssp-function"></a>AcceptSecurityContext-Funktion (CredSSP)

Mit **der Funktion AcceptSecurityContext (CredSSP)** kann die Serverkomponente einer Transportanwendung einen Sicherheitskontext zwischen dem Server und einem Remoteclient einrichten. Der Remoteclient ruft die [**Funktion InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) auf, um den Prozess zum Einrichten eines Sicherheitskontexts zu starten. Der Server kann mindestens ein Antworttoken vom Remoteclient benötigen, um die Einrichtung des Sicherheitskontexts abschließen zu können.

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

*phCredential* \[ in, optional\]

Ein Handle für die Serveranmeldeinformationen. Um dieses Handle abzurufen, ruft der Server die [**Funktion AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) auf, bei der entweder das SECPKG \_ CRED \_ INBOUND- oder SECPKG CRED BOTH-Flag festgelegt \_ \_ ist.

*phContext* \[ in, optional\]

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (CredSSP)** ist dieser Zeiger **NULL.** Bei nachfolgenden Aufrufen *gibt phContext* den teilweise gebildeten Kontext an, der durch den ersten Aufruf im *phNewContext-Parameter* zurückgegeben wird.

*pInput* \[ in, optional\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die durch einen Clientaufruf von [**InitializeSecurityContext (CredSSP) generiert wird.**](initializesecuritycontext--credssp.md) Die -Struktur enthält den Eingabepufferdeskriptor.

Der erste Puffer muss vom Typ **SECBUFFER \_ TOKEN** sein und das vom Client empfangene Sicherheitstoken enthalten. Der zweite Puffer muss vom Typ **SECBUFFER \_ EMPTY sein.**

*fContextReq* \[ In\]

-Bit-Flags, die die Attribute angeben, die der Server zum Einrichten des Kontexts benötigt. Bitflags können mithilfe bitweiser **OR-Vorgänge kombiniert** werden. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.

| Wert                          | Bedeutung                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ \_ REQ– SPEICHER \_ ZUWEISEN** | Der Credential Security Support Provider (CredSSP) ordnet Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie sie frei, indem Sie die [**FreeContextBuffer-Funktion**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) aufrufen. |
| **ASC \_ \_ REQ-VERBINDUNG**       | Der Sicherheitskontext verarbeitet keine Formatierungsmeldungen.                                                                                                                                                      |
| **\_ASC-REQ-DELEGAT \_**         | Der Server darf die Identität des Clients imitieren. Ignorieren Sie dieses Flag für die eingeschränkte Delegierung.                                                         |
| **ERWEITERTER ASC \_ \_ \_ REQ-FEHLER**  | Wenn Fehler auftreten, wird die Remote-Partei benachrichtigt.                                                                                                                                                          |
| **ASC \_ REQ \_ REPLAY \_ DETECT**   | Erkennen von wiedergegebenen Paketen.                                                                                                                                                                                       |
| **ASC \_ REQ \_ SEQUENCE \_ DETECT** | Erkennen von Nachrichten, die nicht sequenziert empfangen werden.                                                                                                                                                                      |
| **ASC \_ REQ \_ STREAM**           | Unterstützt eine streamorientierte Verbindung.                                                                                                                                                                          |

Mögliche Attributflags und deren Bedeutung finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC REQ, z. B. \_ ASC \_ REQ \_ DELEGATE.

Die angeforderten Attribute werden vom Client möglicherweise nicht unterstützt. Weitere Informationen finden Sie unter dem *parameter pfContextAttr.*

*TargetDataRep* \[ In\]

Die Datendarstellung, z. B. die Byte reihenfolge, auf dem Ziel. Dieser Parameter kann entweder **SECURITY \_ NATIVE \_ DREP oder** SECURITY NETWORK **\_ \_ DREP sein.**

*phNewContext* \[ in, out, optional\]

Ein Zeiger auf eine [CTXTHandle-Struktur.](sspi-handles.md) Beim ersten Aufruf von **AcceptSecurityContext (CredSSP)** empfängt dieser Zeiger das neue Kontexthand handle. Bei nachfolgenden Aufrufen *kann phNewContext* mit dem im *phContext-Parameter* angegebenen Handle identisch sein.

*pOutput* \[ in, out, optional\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) die den Ausgabepufferdeskriptor enthält. Dieser Puffer wird zur Eingabe in zusätzliche Aufrufe von [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)an den Client gesendet. Ein Ausgabepuffer kann auch dann generiert werden, wenn die Funktion SEC \_ E \_ OK zurückgibt. Alle generierten Puffer müssen zurück an die Clientanwendung gesendet werden.

Bei der Ausgabe empfängt dieser Puffer ein Token für den Sicherheitskontext. Das Token muss an den Client gesendet werden. Die Funktion kann auch einen Puffer vom Typ SECBUFFER \_ EXTRA zurückgeben.

*pfContextAttr* \[ out\]

Ein Zeiger auf einen Satz von Bitflags, die die Attribute des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md) Flags, die für diesen Parameter verwendet werden, haben das Präfix ASC RET, z. \_ B. ASC \_ RET \_ DELEGATE.

Überprüfen Sie erst nach sicherheitsbezogenen Attributen, wenn der letzte Funktionsaufruf erfolgreich zurückgegeben wird. Attributflags, die sich nicht auf die Sicherheit bezieht, z. B. das ASC \_ RET ALLOCATED MEMORY-Flag, können vor der \_ \_ endgültigen Rückgabe überprüft werden.

*ptsExpiry* \[ out, optional\]

Ein Zeiger auf eine [**TimeStamp-Struktur,**](timestamp.md) die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das Sicherheitspaket diesen Wert immer in Ortszeit zurück gibt.

> [!Note]  
> Bis zum letzten Aufruf des Authentifizierungsprozesses kann die Ablaufzeit für den Kontext falsch sein, da in späteren Phasen der Aushandlung weitere Informationen bereitgestellt werden. Daher muss *ptsTimeStamp* bis zum letzten Aufruf der Funktion **NULL** sein.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.

| Rückgabecode/-wert                                   | Beschreibung                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | Die Funktion wurde erfolgreich ausgeführt. Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss zusätzliche Daten vom Client lesen und [<strong>AcceptSecurityContext (CredSSP) erneut</strong>](acceptsecuritycontext--credssp.md) aufrufen. |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | Fehler bei der Funktion. Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | Fehler bei der Funktion. Es ist ein Fehler aufgetreten, der einem SSPI-Fehlercode nicht zuordnen konnte.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | Fehler bei der Funktion. Das an die Funktion übergebene Handle ist ungültig.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | Fehler bei der Funktion. Das an die Funktion übergebene Token ist ungültig.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Fehler bei der Anmeldung.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | Fehler bei der Funktion. Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Dies kann folgende Bedingungen haben:<br/><ul><li>Der Domänenname der authentifizierenden Partei ist falsch.</li><li>Die Domäne ist nicht verfügbar.</li><li>Die Vertrauensstellung ist fehlgeschlagen. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | Fehler bei der Funktion. Das im *phCredential-Parameter angegebene Anmeldeinformationshandl* ist ungültig.                            |
| SEC_E_OK <br/> 0x00000000L                          | Die Funktion wurde erfolgreich ausgeführt. Der vom Client empfangene Sicherheitskontext wurde akzeptiert. Wenn die Funktion ein Ausgabetoken generiert hat, muss das Token an den Clientprozess gesendet werden. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | Fehler bei der Funktion. Der *fContextReq-Parameter* hat ein ungültiges Kontextattributflag (ASC_REQ_DELEGATE oder ASC_REQ_PROMPT_FOR_CREDS) angegeben.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | Die Funktion wurde erfolgreich ausgeführt. Der Server muss [**CompleteAuthToken aufrufen**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) und das Ausgabetoken an den Client übergeben. Der Server muss dann auf ein Rückgabetoken vom Client warten, bevor ein weiterer Aufruf von [**AcceptSecurityContext (CredSSP) ausgeführt wird.**](acceptsecuritycontext--credssp.md) |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Erstellen der Nachricht vom Client beenden, bevor [ **CompleteAuthToken aufruft.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | Die Funktion wurde erfolgreich ausgeführt. Der Server muss das Ausgabetoken an den Client senden und auf ein zurückgegebenes Token warten. Das zurückgegebene Token sollte in *pInput für einen* weiteren Aufruf von [**AcceptSecurityContext (CredSSP) übergeben werden.**](acceptsecuritycontext--credssp.md)


## <a name="remarks"></a>Hinweise

Die **Funktion AcceptSecurityContext (CredSSP)** ist das Server-Pendant zur [**InitializeSecurityContext-Funktion (CredSSP).**](initializesecuritycontext--credssp.md)

Wenn der Server eine Anforderung von einem Client empfängt, verwendet er den *Parameter fContextReq,* um anzugeben, was für die Sitzung erforderlich ist. Auf diese Weise kann ein Server verlangen, dass Clients [](../secgloss/i-gly.md)eine vertrauliche oder integritätsgeprüfte Sitzung verwenden können. Sie kann Clients ablehnen, die diese Anforderung nicht erfüllen können. Alternativ kann ein Server nichts benötigen. Alles, was der Client erfordert oder bereitstellen kann, wird im *parameter pfContextAttr* zurückgegeben.

Die *Parameter fContextReq* und *pfContextAttr* sind Bitmasken, die verschiedene Kontextattribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontextanforderungen.](context-requirements.md)

> [!Note]  
> Obwohl der *parameter pfContextAttr* bei jeder erfolgreichen Rückgabe gültig ist, sollten Sie die Flags im Zusammenhang mit Sicherheitsaspekten des Kontexts nur bei der endgültigen erfolgreichen Rückgabe untersuchen. Zwischenrück rückgaben können z. B. das ISC \_ RET \_ ALLOCATED \_ MEMORY-Flag festlegen.

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die endgültigen Kontextattribute ausreichend sind. Wenn beispielsweise Vertraulichkeit (Verschlüsselung) angefordert wurde, aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort herunterfahren. Wenn der Sicherheitskontext nicht eingerichtet werden kann, muss der Server den teilweise erstellten Kontext durch Aufrufen der [**DeleteSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) frei geben. Informationen dazu, wann die **DeleteSecurityContext-Funktion aufgerufen werden** soll, finden Sie unter **DeleteSecurityContext**.

Nachdem der Sicherheitskontext eingerichtet wurde, kann die Serveranwendung die [**QuerySecurityContextToken-Funktion**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) verwenden, um ein Handle für das Benutzerkonto abzurufen, dem das Clientzertifikat zugeordnet wurde. Außerdem kann der Server die [**ImpersonateSecurityContext-Funktion**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) verwenden, um die Identität des Benutzers zu ändern.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[ Vista-Desktop-Apps\]       |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2008-Desktop-Apps\] |
| Header                   | Sspi.h (einschließlich Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Weitere Informationen

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
