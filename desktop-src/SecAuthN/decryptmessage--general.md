---
description: Entschlüsselt eine Nachricht.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: DecryptMessage(General)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9dfbde6c0b4a8c46920428af3d7f700268f11690
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476916"
---
# <a name="decryptmessage-general-function"></a>DecryptMessage(General)-Funktion

Die **DecryptMessage (General)-Funktion** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen stattdessen einen [*Integritätshash*](../secgloss/h-gly.md)aus und überprüfen sie.

Der [*Digestsicherheits-Supportanbieter*](../secgloss/s-gly.md) (SSP) bietet Verschlüsselungs- und Entschlüsselungsvertraulichkeit für Nachrichten, die zwischen Client und Server als SASL-Mechanismus ausgetauscht werden.

Diese Funktion wird auch mit dem Schannel-SSP verwendet, um eine Anforderung von einem Nachrichtensender für eine Neuaushandlung (Wiederholung) der Verbindungsattribute oder für das Herunterfahren der Verbindung zu signalisieren.

> [!Note]  
> [**EncryptMessage (Allgemein)**](encryptmessage--general.md) und **DecryptMessage (Allgemein)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

 

Informationen zur Verwendung dieser Funktion mit einem bestimmten SSP finden Sie in den folgenden Themen.



| Thema                                                            | BESCHREIBUNG                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (Digest)**](decryptmessage--digest.md)       | Entschlüsselt eine Nachricht mithilfe von Digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Entschlüsselt eine Nachricht mit kerberos.  |
| [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) | Entschlüsselt eine Nachricht mit negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Entschlüsselt eine Nachricht mit NTLM.      |
| [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)   | Entschlüsselt eine Nachricht mithilfe von Schannel.  |



 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phContext* \[ In\]
</dt> <dd>

Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md) der zum Entschlüsseln der Nachricht verwendet werden soll.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Daten kann vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird vor Ort entschlüsselt und überschreibt den ursprünglichen Inhalt des Puffers.

Bei Verwendung des Digest-SSP verweist die Struktur bei der Eingabe auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Nachrichten muss vom Typ SECBUFFER \_ DATA oder SECBUFFER STREAM sein und die verschlüsselte Nachricht \_ enthalten.

Wenn Sie den Schannel-SSP mit Kontexten verwenden, die nicht verbindungsorientiert sind, muss die -Struktur bei der Eingabe vier [**SecBuffer-Strukturen**](/windows/win32/api/sspi/ns-sspi-secbuffer) enthalten. Genau ein Puffer muss vom Typ SECBUFFER DATA sein \_ und eine verschlüsselte Nachricht enthalten, die vor Ort entschlüsselt wird. Die verbleibenden Puffer werden für die Ausgabe verwendet und müssen vom Typ SECBUFFER \_ EMPTY sein. Für verbindungsorientierte Kontexte muss ein \_ SECBUFFER-DATENTYPpuffer bereitgestellt werden, wie für nicht verbindungsorientierte Kontexte angegeben. Darüber hinaus muss ein zweiter SECBUFFER \_ TOKEN-Typpuffer angegeben werden, der ein Sicherheitstoken enthält.

</dd> <dt>

*MessageSeqNo* \[ In\]
</dt> <dd>

Die von der Transportanwendung erwartete Sequenznummer, sofern vorhanden. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenznummerierung intern.

Wenn Sie den Schannel-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

</dd> <dt>

*pfQOP* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Bei Verwendung des Schannel-SSP wird dieser Parameter nicht verwendet und sollte auf **NULL** festgelegt werden.

Dieser Parameter kann eines der folgenden Flags sein.




| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Die Nachricht wurde nicht verschlüsselt, aber ein Header oder Nachspann wurde erstellt.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Wenn Sie den Digest-SSP verwenden, verwenden Sie dieses Flag, wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) festgelegt ist, um nur die [*Signatur*](../secgloss/s-gly.md) zu überprüfen. Weitere Informationen finden Sie unter [Quality of Protection](quality-of-protection.md).<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ BUFFER \_ TOO \_ SMALL**</dt> </dl>      | Der Nachrichtenpuffer ist zu klein. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ INCOMPLETE \_ MESSAGE**</dt> </dl>     | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Allgemein)**](decryptmessage--general.md) erneut aufrufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Ein ungültiges Kontexthandle wurde im *phContext-Parameter* angegeben. Wird mit den Digest- und Schannel-SSPs verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ E \_ INVALID \_ TOKEN**</dt> </dl>          | Die Puffer haben den falschen Typ, oder es wurde kein Puffer vom Typ SECBUFFER \_ DATA gefunden. Wird mit dem Schannel-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ MESSAGE \_ ALTERED**</dt> </dl>        | Die Nachricht wurde geändert. Wird mit den Digest- und Schannel-SSPs verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ OUT \_ OF \_ SEQUENCE**</dt> </dl>       | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**</dt> </dl>     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ I \_ CONTEXT \_ EXPIRED**</dt> </dl>        | Der Absender der Nachricht hat die Verbindung beendet und das Herunterfahren initiiert. Informationen zum Initiieren oder Erkennen eines Herunterfahrens finden Sie unter [Herunterfahren einer Schannel-Verbindung.](shutting-down-an-schannel-connection.md) Wird mit dem Schannel-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ I \_ NEU AUSHANDELN**</dt> </dl>             | Die Remotepartei erfordert eine neue Handshakesequenz, oder die Anwendung hat gerade das Herunterfahren initiiert. Kehren Sie zur Aushandlungsschleife zurück, und rufen [**Sie AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) oder [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md)auf, und übergeben Sie leere Eingabepuffer. <br/> Wenn die Funktion einen Puffer vom Typ **SEC \_ BUFFER \_ EXTRA** zurückgibt, sollte dieser als Eingabepuffer an die [**AcceptSecurityContext (General)-Funktion**](acceptsecuritycontext--general.md) übergeben werden.<br/> Wird mit dem Schannel-SSP verwendet.<br/> Neuverhandlung wird für den Schannel-Kernelmodus nicht unterstützt. Der Aufrufer sollte diesen Rückgabewert entweder ignorieren oder die Verbindung beenden. Wenn der Wert ignoriert wird, kann entweder der Client oder der Server die Verbindung als Ergebnis herunterfahren.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie den Schannel-SSP verwenden, gibt die **DecryptMessage (General)-Funktion** SEC \_ I CONTEXT EXPIRED \_ \_ zurück, wenn der Absender der Nachricht die Verbindung beendet hat. Informationen zum Initiieren oder Erkennen eines Herunterfahrens finden Sie unter [Herunterfahren einer Schannel-Verbindung.](shutting-down-an-schannel-connection.md)

Wenn Sie den Schannel-SSP verwenden, gibt **DecryptMessage (Allgemein)** SEC \_ I \_ MOONGOTIATE zurück, wenn der Absender der Nachricht die Verbindung neu aushandeln möchte ([*Sicherheitskontext*](../secgloss/s-gly.md)). Eine Anwendung verarbeitet eine angeforderte Neuverhandlung, indem [**AcceptSecurityContext (Allgemein) (serverseitig)**](acceptsecuritycontext--general.md) oder [**InitializeSecurityContext (allgemein) (clientseitig)**](initializesecuritycontext--general.md) aufgerufen und leere Eingabepuffer übergeben werden. Nachdem dieser anfängliche Aufruf einen Wert zurückgegeben hat, fahren Sie so fort, als würde Ihre Anwendung eine neue Verbindung erstellen. Weitere Informationen finden Sie unter [Erstellen eines Schannel-Sicherheitskontexts. [](../secgloss/s-gly.md)](creating-an-schannel-security-context.md)

Informationen zur Interoperabilität mit GSSAPI finden Sie unter [SSPI-/Kerberos-Interoperabilität mit GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

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

[**EncryptMessage (Allgemein)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
