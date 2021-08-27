---
description: Verschlüsselt eine Nachricht zur Bereitstellung von Datenschutz mit ntlm.
ms.assetid: 852a4624-792d-4f7d-bd3e-5a28692e2ef3
title: EncryptMessage-Funktion (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5c36ce31793a7dc889b6dec40acac7606cc38bf3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480806"
---
# <a name="encryptmessage-ntlm-function"></a>EncryptMessage-Funktion (NTLM)

Die **Funktion EncryptMessage (NTLM)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. **EncryptMessage (NTLM)** ermöglicht einer Anwendung die Auswahl zwischen [*kryptografischen Algorithmen,*](../secgloss/c-gly.md) die vom ausgewählten Mechanismus unterstützt werden. Die **EncryptMessage -Funktion (NTLM)** verwendet den [*Sicherheitskontext,*](../secgloss/s-gly.md) auf den das Kontexthandle verweist. Einige Pakete verfügen nicht über Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen [*Integritätshash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

> [!Note]  
> **EncryptMessage (NTLM)** und [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) können gleichzeitig von zwei verschiedenen Threads in einem einzelnen SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

## <a name="syntax"></a>Syntax

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a>Parameter

*phContext* \[ In\]

Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md) der zum Verschlüsseln der Nachricht verwendet werden soll.

*fQOP* \[ In\]

Paketspezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl [*kryptografischer Algorithmen*](../secgloss/c-gly.md)zu aktivieren.

Dieser Parameter kann das folgende Flag sein.


| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Erstellen Sie einen Header oder Nachspann, aber verschlüsseln Sie die Nachricht nicht.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 


*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die vom Typ SECBUFFER DATA sein \_ können. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird an Ort und Stelle verschlüsselt und überschreibt den ursprünglichen Inhalt der -Struktur.

Die Funktion verarbeitet keine Puffer mit dem SECBUFFER \_ READONLY-Attribut.

Die Länge der [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Nachricht enthält, darf nicht größer als **cbMaximumMessage** sein, die von der [**Funktion QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) (SECPKG \_ ATTR STREAM SIZES) abgerufen \_ \_ wird.

Anwendungen, die SSL nicht verwenden, müssen einen [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ SECBUFFER \_ PADDING bereitstellen.

*MessageSeqNo* \[ In\]

Die Sequenznummer, die die Transportanwendung der Nachricht zugewiesen hat. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter 0 (null) sein.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ BUFFER \_ TOO \_ SMALL**      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                   |
| **SEC \_ E \_ CONTEXT \_ EXPIRED**        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Eine ordnungsgemäß geschriebene Anwendung sollte diesen Fehler nicht erhalten. |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt.                                |
| **SEC \_ E \_ INSUFFICIENT \_ MEMORY**    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                               |
| **SEC \_ E \_ INVALID \_ HANDLE**         | Im *phContext-Parameter* wurde ein ungültiges Kontexthandle angegeben.                                                       |
| **SEC \_ E \_ INVALID \_ TOKEN**          | Es wurde kein \_ SECBUFFER-DATENTYPpuffer gefunden.                                                                                            |
| **SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**>    | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt.             |

## <a name="remarks"></a>Hinweise

Die **Funktion EncryptMessage (NTLM)** verschlüsselt eine Nachricht basierend auf der Nachricht und dem [*Sitzungsschlüssel*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext.*](../secgloss/s-gly.md)

Wenn die Transportanwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenzerkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die Funktion diese Informationen mit der verschlüsselten Nachricht. Das Einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transportanwendung übergeben wird.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_SECBUFFER-STREAMHEADER \_  | Wird intern verwendet. Keine Initialisierung erforderlich.                                                |
| SECBUFFER \_ DATA            | Enthält die zu verschlüsselnde [*Klartextnachricht.*](../secgloss/s-gly.md) |
| SECBUFFER \_ STREAM \_ TRAILER | Wird intern verwendet. Keine Initialisierung erforderlich.                                                |
| SECBUFFER \_ EMPTY           | Wird intern verwendet. Keine Initialisierung erforderlich. Die Größe kann 0 (null) sein.                              |

Um eine optimale Leistung zu erzielen, sollten die *pMessage-Strukturen* aus zusammenhängendem Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als **SealMessage** bezeichnet. Anwendungen sollten jetzt nur **EncryptMessage (NTLM)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
| -------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[Nur XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (include Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Weitere Informationen

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md)
- [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)
- [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)
- [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
