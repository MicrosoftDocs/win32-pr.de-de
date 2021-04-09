---
description: Entschlüsselt eine Nachricht mithilfe von Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: DecryptMessage (Kerberos)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129925"
---
# <a name="decryptmessage-kerberos-function"></a>DecryptMessage (Kerberos)-Funktion

Mit der **DecryptMessage (Kerberos)** -Funktion wird eine Nachricht entschlüsselt. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.

> [!Note]  
> " [**Verschlüsseltmessage (Kerberos)**](encryptmessage--kerberos.md) " und " **DecryptMessage" (Kerberos)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ "secbuffer Data" aufweisen können \_ . Der Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.

*Messageseqno* \[ in\]

Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.

*pfqop* \[ vorgenommen\]

Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.

Dieser Parameter kann das folgende Flag aufweisen.

| Wert                  | Bedeutung                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                     | Beschreibung                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sekunde \_ E \_ unvollständige \_ Nachricht** | Die Daten im Eingabepuffer sind unvollständig. Die Anwendung muss weitere Daten vom Server lesen und [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) erneut aufzurufen. |
| **Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                                                                                            |

## <a name="remarks"></a>Bemerkungen

Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (Kerberos)** zu entschlüsseln, und ermittelt, dass **DecryptMessage (Kerberos)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.

Weitere Informationen zum interagieren mit GSSAPI finden Sie unter [SSPI/Kerberos-Interoperabilität mit GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

**Windows XP:** Diese Funktion wurde auch als **unversiemessage** bezeichnet. Anwendungen sollten jetzt nur **DecryptMessage (Kerberos)** verwenden.

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
- [**Verschlüsselungs Meldung (Kerberos)**](encryptmessage--kerberos.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
