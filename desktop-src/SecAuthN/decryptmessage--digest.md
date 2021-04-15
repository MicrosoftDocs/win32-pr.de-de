---
description: Entschlüsselt eine Nachricht mit Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage (Digest)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5363a5efc79d78c9c88e4a817c1c341e0e0f9c02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485254"
---
# <a name="decryptmessage-digest-function"></a>DecryptMessage (Digest)-Funktion

Mit der **DecryptMessage (Digest)** -Funktion wird eine Nachricht entschlüsselt. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.

Die Digest- [*Security Support Provider*](../secgloss/s-gly.md) (SSP) ermöglicht die Verschlüsselung und Entschlüsselung von Nachrichten, die zwischen Client und Server als SASL-Mechanismus ausgetauscht werden.

> [!Note]  
> [**Verschlüsseltmessage (Digest)**](encryptmessage--digest.md) und **DecryptMessage (Digest)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phcontext* \[ in\]

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Mindestens eine davon muss den Typ "secbuffer Data" aufweisen \_ . Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.

Wenn Sie den Digest-SSP verwenden, verweist die Struktur bei der Eingabe auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eines dieser Typen muss vom Typ "secbuffer \_ Data" oder "secbuffer Stream" sein \_ , und die verschlüsselte Nachricht muss enthalten sein.

*Messageseqno* \[ in\]

Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenz Nummerierung intern.

*pfqop* \[ vorgenommen\]

Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann eines der folgenden Flags sein.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Wenn Sie den Digest-SSP verwenden, verwenden Sie dieses Flag, wenn der [*Sicherheitskontext*](../secgloss/s-gly.md) festgelegt ist, um nur die [*Signatur*](../secgloss/s-gly.md) zu überprüfen. Weitere Informationen finden Sie unter [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sekunde \_ E \_ Puffer \_ zu \_ klein**      | Der Nachrichten Puffer ist zu klein. Wird mit dem Digest-SSP verwendet.                                                                                                                   |
| **s \_ E \_ \_ Kryptografiesystem \_ ungültig** | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt. Wird mit dem Digest-SSP verwendet.                                                                                       |
| **Sekunde \_ E \_ unvollständige \_ Nachricht**     | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Digest)**](decryptmessage--digest.md) erneut aufzurufen. |
| **s \_ E \_ ungültiges \_ handle**         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben. Wird mit dem Digest-SSP verwendet.                                                                     |
| **Sek. \_ E- \_ Nachricht \_ geändert**        | Die Nachricht wurde geändert. Wird mit dem Digest-SSP verwendet.                                                                                                                      |
| **Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**       | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                        |
| **Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt. Wird mit dem Digest-SSP verwendet.                           |

## <a name="remarks"></a>Bemerkungen

Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (Digest)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (Digest)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.

**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet. Anwendungen sollten jetzt nur **DecryptMessage (Digest)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\] |
| Header                   | SSPI. h (Include Security. h)               |
| Bibliothek                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Verschlüsselungs Meldung (Digest)**](encryptmessage--digest.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
