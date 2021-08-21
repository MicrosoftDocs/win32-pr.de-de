---
description: Entschlüsselt eine Nachricht mit kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage-Funktion (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 62add8d4b33f356aeae5bbbf8fa16b19a0b5e419e0ab6c0a6847a3ed087ce726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008538"
---
# <a name="decryptmessage-kerberos-function"></a>DecryptMessage-Funktion (Kerberos)

Die **Funktion DecryptMessage (Kerberos)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln nachrichten nicht, sondern führen stattdessen einen Integritätshash aus und [*überprüfen diesen.*](../secgloss/h-gly.md)

> [!Note]  
> [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) und **DecryptMessage (Kerberos)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phContext* \[ In\]

Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md) der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die vom Typ SECBUFFER DATA sein \_ können. Der Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird an Ort und Stelle entschlüsselt und überschreiben den ursprünglichen Inhalt des Puffers.

*MessageSeqNo* \[ In\]

Die sequenznummer, die von der Transportanwendung erwartet wird, sofern eine davon der Fall ist. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann das folgende Flag sein.

| Wert                  | Bedeutung                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder Nachspann erstellt. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, gibt sie einen der folgenden Fehlercodes zurück.

| Rückgabecode                     | Beschreibung                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ UNVOLLSTÄNDIGE \_ NACHRICHT** | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Kerberos) erneut**](decryptmessage--kerberos.md) aufrufen. |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                            |

## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remote-Partei, versucht, sie mithilfe von **DecryptMessage (Kerberos)** zu entschlüsseln, und festgestellt, dass **DecryptMessage (Kerberos)** erfolgreich war, die Ausgabepuffer jedoch leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen damit umgehen können.

Informationen zur Interoperabilität mit GSSAPI finden Sie unter [SSPI/Kerberos-Interoperabilität mit GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

**Windows XP:** Diese Funktion wurde auch als **UnsealMessage bezeichnet.** Anwendungen sollten jetzt nur **Noch DecryptMessage (Kerberos)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (einschließlich Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
