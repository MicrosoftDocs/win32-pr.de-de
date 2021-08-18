---
description: Entschlüsselt eine Nachricht mit negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage(Negotiate)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 7da05842fc5aba4dc9c19cd530b38e0d46b640aac10b4614981c30c8863d7e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008518"
---
# <a name="decryptmessage-negotiate-function"></a>DecryptMessage(Negotiate)-Funktion

Die **DecryptMessage (Negotiate)-Funktion** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen stattdessen einen [*Integritätshash*](../secgloss/h-gly.md)aus und überprüfen sie.

> [!Note]  
> [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) und **DecryptMessage (Negotiate)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Mindestens eines dieser Daten muss vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird vor Ort entschlüsselt und überschreibt den ursprünglichen Inhalt des Puffers.

*MessageSeqNo* \[ In\]

Die von der Transportanwendung erwartete Sequenznummer, sofern vorhanden. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann das folgende Flag sein.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber ein Header oder Nachspann wurde erstellt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                     | Beschreibung                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ INCOMPLETE \_ MESSAGE** | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) erneut aufrufen. |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                              |

## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remotepartei, versucht, sie mit **decryptMessage (Negotiate)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (Negotiate)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen in der Lage sein, damit umzugehen.

**Windows XP:** Diese Funktion wurde auch als **UnsealMessage** bezeichnet. Anwendungen sollten jetzt nur **DecryptMessage (Negotiate)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[Nur XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (include Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
