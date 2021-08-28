---
description: Entschlüsselt eine Nachricht mithilfe von Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage-Funktion (Digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f87828263766643a10cf5400e38cabe9d3096403
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480866"
---
# <a name="decryptmessage-digest-function"></a>DecryptMessage-Funktion (Digest)

Die **DecryptMessage-Funktion (Digest)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen stattdessen einen [*Integritätshash*](../secgloss/h-gly.md)aus und überprüfen sie.

Der [*Digestsicherheits-Supportanbieter*](../secgloss/s-gly.md) (SSP) bietet Verschlüsselungs- und Entschlüsselungsvertraulichkeit für Nachrichten, die zwischen Client und Server als SASL-Mechanismus ausgetauscht werden.

> [!Note]  
> [**EncryptMessage (Digest)**](encryptmessage--digest.md) und **DecryptMessage (Digest)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

## <a name="syntax"></a>Syntax

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a>Parameter

*phContext* \[ In\]

Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md) der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Mindestens eine davon muss vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird an Ort und Stelle entschlüsselt, und der ursprüngliche Inhalt des Puffers wird überschrieben.

Bei Verwendung des Digest-SSP verweist die Struktur bei der Eingabe auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Nachrichten muss vom Typ SECBUFFER \_ DATA oder SECBUFFER STREAM sein und die verschlüsselte Nachricht \_ enthalten.

*MessageSeqNo* \[ In\]

Die von der Transportanwendung erwartete Sequenznummer, sofern vorhanden. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenznummerierung intern.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann eines der folgenden Flags sein.


| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Die Nachricht wurde nicht verschlüsselt, aber ein Header oder Nachspann wurde erstellt.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Wenn Sie den Digest-SSP verwenden, verwenden Sie dieses Flag, wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) festgelegt ist, um nur die [*Signatur*](../secgloss/s-gly.md) zu überprüfen. Weitere Informationen finden Sie unter [Quality of Protection](quality-of-protection.md).<br /> | 


## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ BUFFER \_ TOO \_ SMALL**      | Der Nachrichtenpuffer ist zu klein. Wird mit dem Digest-SSP verwendet.                                                                                                                   |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt. Wird mit dem Digest-SSP verwendet.                                                                                       |
| **SEC \_ E \_ INCOMPLETE \_ MESSAGE**     | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Digest)**](decryptmessage--digest.md) erneut aufrufen. |
| **SEC \_ E \_ INVALID \_ HANDLE**         | Im *phContext-Parameter* wurde ein ungültiges Kontexthandle angegeben. Wird mit dem Digest-SSP verwendet.                                                                     |
| **SEC \_ E \_ MESSAGE \_ ALTERED**        | Die Nachricht wurde geändert. Wird mit dem Digest-SSP verwendet.                                                                                                                      |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**       | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                        |
| **SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt. Wird mit dem Digest-SSP verwendet.                           |

## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remotepartei, versucht, sie mit **decryptMessage (Digest)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (Digest)** erfolgreich war, die Ausgabepuffer jedoch leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen in der Lage sein, damit umzugehen.

**Windows XP:** Diese Funktion wurde auch als **UnsealMessage** bezeichnet. Anwendungen sollten jetzt nur **DecryptMessage (Digest)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[Nur XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (include Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Weitere Informationen

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
