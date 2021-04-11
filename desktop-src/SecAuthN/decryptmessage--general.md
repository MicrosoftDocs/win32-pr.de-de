---
description: Entschlüsselt eine Meldung.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: DecryptMessage (General)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214822"
---
# <a name="decryptmessage-general-function"></a>DecryptMessage (allgemein)-Funktion

Mit der **DecryptMessage (General)** -Funktion wird eine Nachricht entschlüsselt. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.

Die Digest- [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ermöglicht die Verschlüsselung und Entschlüsselung von Nachrichten, die zwischen Client und Server als SASL-Mechanismus ausgetauscht werden.

Diese Funktion wird auch mit dem Schannel SSP verwendet, um eine Anforderung von einem Nachrichten Absender für eine erneute Aushandlung (Wiederholung) der Verbindungs Attribute oder für das Herunterfahren der Verbindung zu signalisieren.

> [!Note]  
> [**Verschlüsselungsmessage (allgemein)**](encryptmessage--general.md) und **DecryptMessage (allgemein)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

 

Informationen zur Verwendung dieser Funktion mit einem bestimmten SSP finden Sie in den folgenden Themen.



| Thema                                                            | BESCHREIBUNG                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (Digest)**](decryptmessage--digest.md)       | Entschlüsselt eine Nachricht mit Digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Entschlüsselt eine Nachricht mithilfe von Kerberos.  |
| [**DecryptMessage (aushandeln)**](decryptmessage--negotiate.md) | Entschlüsselt eine Nachricht mithilfe von "aushandeln". |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Entschlüsselt eine Nachricht mithilfe von NTLM.      |
| [**DecryptMessage (SChannel)**](decryptmessage--schannel.md)   | Entschlüsselt eine Nachricht mithilfe von Schannel.  |



 

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

*phcontext* \[ in\]
</dt> <dd>

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eine dieser Typen kann vom Typ "secbuffer \_ Data" sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.

Wenn Sie den Digest-SSP verwenden, verweist die Struktur bei der Eingabe auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eines dieser Typen muss vom Typ "secbuffer \_ Data" oder "secbuffer Stream" sein \_ , und die verschlüsselte Nachricht muss enthalten sein.

Wenn der Schannel-SSP mit Kontexten verwendet wird, die nicht verbindungsorientiert sind, muss die Struktur bei der Eingabe vier [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen enthalten. Genau ein Puffer muss den Typ "secbuffer \_ Data" aufweisen und eine verschlüsselte Nachricht enthalten, die an Ort und Stelle entschlüsselt wird. Die restlichen Puffer werden für die Ausgabe verwendet und müssen den Typ "secbuffer Empty" aufweisen \_ . Bei Verbindungs orientierten Kontexten muss ein secbuffer \_ -Datentyp Puffer angegeben werden, wie für nicht Verbindungs orientierte Kontexte angegeben. Darüber hinaus muss auch ein zweiter Typ eines secbuffer- \_ Tokentyps, der ein Sicherheits Token enthält, bereitgestellt werden.

</dd> <dt>

*Messageseqno* \[ in\]
</dt> <dd>

Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenz Nummerierung intern.

Bei Verwendung des Schannel-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

</dd> <dt>

*pfqop* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.

Wenn der Schannel SSP verwendet wird, wird dieser Parameter nicht verwendet und sollte auf **null** festgelegt werden.

Dieser Parameter kann eines der folgenden Flags sein.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Wenn Sie den Digest-SSP verwenden, verwenden Sie dieses Flag, wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) festgelegt ist, um nur die [*Signatur*](../secgloss/s-gly.md) zu überprüfen. Weitere Informationen finden Sie unter [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt> </dl>      | Der Nachrichten Puffer ist zu klein. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt> </dl> | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Sekunde \_ E \_ unvollständige \_ Nachricht**</dt> </dl>     | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (allgemein)**](decryptmessage--general.md) erneut aufzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben. Wird mit dem Digest-und SChannel-SSPs verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>          | Die Puffer weisen den falschen Typ auf, oder es wurde kein Puffer vom Typ "secbuffer \_ Data" gefunden. Wird mit dem Schannel SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**Sek. \_ E- \_ Nachricht \_ geändert**</dt> </dl>        | Die Nachricht wurde geändert. Wird mit dem Digest-und SChannel-SSPs verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**</dt> </dl>       | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt> </dl>     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt. Wird mit dem Digest-SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**Sek., \_ \_ Kontext \_ abgelaufen**</dt> </dl>        | Der Absender der Nachricht hat die Verbindung nicht mehr hergestellt und hat ein Herunterfahren initiiert. Informationen zum initiieren oder erkennen eines herunter Fahrens finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md). Wird mit dem Schannel SSP verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**Sekunde, die \_ ich erneut \_ verhandate**</dt> </dl>             | Die Remote Partei benötigt eine neue Hand Shake Sequenz, oder die Anwendung hat gerade ein Herunterfahren initiiert. Kehren Sie zur Aushandlungs Schleife zurück, und geben Sie " [**akzeptsecuritycontext (allgemein)**](acceptsecuritycontext--general.md) " oder " [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md)" an, indem Sie leere Eingabepuffer übergeben. <br/> Wenn die Funktion einen Puffer vom Typ " **sec- \_ Puffer \_ extra**" zurückgibt, sollte dieser als Eingabepuffer an die Funktion " [**akzeptsecuritycontext (allgemein)**](acceptsecuritycontext--general.md) " übermittelt werden.<br/> Wird mit dem Schannel SSP verwendet.<br/> Die Neuverhandlung wird für den SChannel-Kernel Modus nicht unterstützt. Der Aufrufer sollte entweder diesen Rückgabewert ignorieren oder die Verbindung beenden. Wenn der Wert ignoriert wird, kann die Verbindung entweder vom Client oder vom Server beendet werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie Schannel SSP verwenden, gibt die Funktion **DecryptMessage (allgemein)** den Wert Sekunde zurück, den der \_ \_ Kontext \_ abgelaufen ist, wenn der Absender der Nachricht die Verbindung beendet hat. Informationen zum initiieren oder erkennen eines herunter Fahrens finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md).

Wenn Sie Schannel SSP verwenden, gibt **DecryptMessage (allgemein)** Sekunde zurück, die \_ ich \_ neu aushandeln muss, wenn der Absender der Nachricht die Verbindung erneut aushandeln möchte ([*Sicherheitskontext*](../secgloss/s-gly.md)). Eine Anwendung verarbeitet eine angeforderte Neuverhandlung durch Aufrufen von " [**Accept-SecurityContext (allgemein)**](acceptsecuritycontext--general.md) (serverseitig)" oder " [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md) " (Client seitig) und durch Übergabe leerer Eingabepuffer. Nachdem dieser anfängliche-Befehl einen Wert zurückgegeben hat, fahren Sie so fort, als ob die Anwendung eine neue Verbindung erstellt hat. Weitere Informationen finden Sie unter [Erstellen eines SChannel- [*Sicherheits Kontexts*](../secgloss/s-gly.md)](creating-an-schannel-security-context.md).

Weitere Informationen zum interagieren mit GSSAPI finden Sie unter [SSPI/Kerberos-Interoperabilität mit GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

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

[**Verschlüsselungsnachricht (allgemein)**](encryptmessage--general.md)
</dt> <dt>

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
