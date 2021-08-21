---
description: Entschlüsselt eine Nachricht mithilfe von Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage-Funktion (Digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: c9ea0cc2f0ea0cbe10a91ba48fd7d6396532fd1867d9fe84043aa008df507446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008628"
---
# <a name="decryptmessage-digest-function"></a>DecryptMessage-Funktion (Digest)

Die **DecryptMessage-Funktion (Digest)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln nachrichten nicht, sondern führen stattdessen einen Integritätshash aus und [*überprüfen diesen.*](../secgloss/h-gly.md)

Der SSP (Digest [*Security Support Provider)*](../secgloss/s-gly.md) bietet Verschlüsselungs- und Entschlüsselungsgeheimnisse nur für Nachrichten, die zwischen Client und Server als SASL-Mechanismus ausgetauscht werden.

> [!Note]  
> [**EncryptMessage (Digest)**](encryptmessage--digest.md) und **DecryptMessage (Digest)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Mindestens eine dieser Typen muss vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird an Ort und Stelle entschlüsselt und überschreiben den ursprünglichen Inhalt des Puffers.

Bei Verwendung des Digest-SSP verweist die Struktur bei der Eingabe auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Typen muss vom Typ SECBUFFER DATA oder \_ SECBUFFER STREAM sein und die verschlüsselte Nachricht \_ enthalten.

*MessageSeqNo* \[ In\]

Die sequenznummer, die von der Transportanwendung erwartet wird, sofern eine davon der Fall ist. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenznummerierung intern.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann eines der folgenden Flags sein.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder Nachspann erstellt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Wenn Sie den Digest-SSP verwenden, verwenden Sie dieses Flag, [*wenn*](../secgloss/s-gly.md) der Sicherheitskontext so festgelegt ist, dass nur die [*Signatur überprüft*](../secgloss/s-gly.md) wird. Weitere Informationen finden Sie unter [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, gibt sie einen der folgenden Fehlercodes zurück.

| Rückgabecode                         | Beschreibung                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ BUFFER \_ TOO \_ SMALL**      | Der Nachrichtenpuffer ist zu klein. Wird mit dem Digest-SSP verwendet.                                                                                                                   |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | Die [*für den*](../secgloss/c-gly.md) Sicherheitskontext ausgewählte Verschlüsselung wird nicht unterstützt. [](../secgloss/s-gly.md) Wird mit dem Digest-SSP verwendet.                                                                                       |
| **SEC \_ E \_ UNVOLLSTÄNDIGE \_ NACHRICHT**     | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Digest) erneut**](decryptmessage--digest.md) aufrufen. |
| **SEC \_ E \_ UNGÜLTIGES \_ HANDLE**         | Im *phContext-Parameter* wurde ein ungültiges Kontexthand handle angegeben. Wird mit dem Digest-SSP verwendet.                                                                     |
| **SEC \_ E \_ MESSAGE \_ ALTERED**        | Die Nachricht wurde geändert. Wird mit dem Digest-SSP verwendet.                                                                                                                      |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**       | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                        |
| **SEC \_ E \_ QOP \_ NOT \_ SUPPORTED**     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext unterstützt.*](../secgloss/s-gly.md) Wird mit dem Digest-SSP verwendet.                           |

## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remote-Partei, versucht, sie mithilfe von **DecryptMessage (Digest)** zu entschlüsseln, und festgestellt, dass **DecryptMessage (Digest)** erfolgreich war, die Ausgabepuffer jedoch leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen damit umgehen können.

**Windows XP:** Diese Funktion wurde auch als **UnsealMessage bezeichnet.** Anwendungen sollten jetzt nur **DecryptMessage (Digest)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (einschließlich Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
