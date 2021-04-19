---
description: Entschlüsselt eine Nachricht mithilfe von "aushandeln".
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (aushandeln)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360088"
---
# <a name="decryptmessage-negotiate-function"></a>DecryptMessage (aushandeln)-Funktion

Mit der **DecryptMessage (Aushandlungs)** -Funktion wird eine Nachricht entschlüsselt. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.

> [!Note]  
> [**Verschlüsselungsmessage (aushandeln)**](encryptmessage--negotiate.md) und **DecryptMessage (aushandeln)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phcontext* \[ in\]

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Mindestens eine davon muss den Typ "secbuffer Data" aufweisen \_ . Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.

*Messageseqno* \[ in\]

Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.

*pfqop* \[ vorgenommen\]

Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann das folgende Flag aufweisen.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                     | Beschreibung                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sekunde \_ E \_ unvollständige \_ Nachricht** | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (aushandeln)**](decryptmessage--negotiate.md) erneut aufzurufen. |
| **Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                              |

## <a name="remarks"></a>Bemerkungen

Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (aushandeln)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (aushandeln)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.

**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet. Anwendungen sollten jetzt nur **DecryptMessage (aushandeln)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\] |
| Header                   | SSPI. h (Include Security. h)               |
| Bibliothek                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Verschlüsselungsnachricht (aushandeln)**](encryptmessage--negotiate.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
