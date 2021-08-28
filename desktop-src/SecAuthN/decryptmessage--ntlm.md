---
description: Entschlüsselt eine Nachricht mit NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: DecryptMessage-Funktion (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f73159c1b6e9fbe3d6d9c282ffdb05271e29583b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481046"
---
# <a name="decryptmessage-ntlm-function"></a>DecryptMessage-Funktion (NTLM)

Die **DecryptMessage-Funktion (NTLM)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen stattdessen einen [*Integritätshash*](../secgloss/h-gly.md)aus und überprüfen sie.

> [!Note]  
> [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) und **DecryptMessage (NTLM)** können gleichzeitig von zwei verschiedenen Threads in einem einzelnen SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Mindestens eine davon muss vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird an Ort und Stelle entschlüsselt, und der ursprüngliche Inhalt des Puffers wird überschrieben.

*MessageSeqNo* \[ In\]

Die von der Transportanwendung erwartete Sequenznummer, sofern vorhanden. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann das folgende Flag sein.


| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Die Nachricht wurde nicht verschlüsselt, aber ein Header oder Nachspann wurde erstellt.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 


## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                     | Beschreibung                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ INCOMPLETE \_ MESSAGE** | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) erneut aufrufen. |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                    |

## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remotepartei, versucht, sie mithilfe von **DecryptMessage (NTLM)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (NTLM)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen in der Lage sein, damit umzugehen.

**Windows XP:** Diese Funktion wurde auch als **UnsealMessage** bezeichnet. Anwendungen sollten jetzt nur **noch DecryptMessage (NTLM)** verwenden.

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
- [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
