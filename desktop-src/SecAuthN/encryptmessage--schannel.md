---
description: Verschlüsselt eine Nachricht, um Datenschutz mithilfe von Schannel bereitzustellen.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: EncryptMessage-Funktion (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: de792e543a8cb67bd6b608d79832fd31a68267fc297a85e0e178d268bbc069d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008288"
---
# <a name="encryptmessage-schannel-function"></a>EncryptMessage-Funktion (Schannel)

Die **Funktion EncryptMessage (Schannel)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. **EncryptMessage (Schannel)** ermöglicht einer Anwendung die Auswahl zwischen [*kryptografischen Algorithmen,*](../secgloss/c-gly.md) die vom ausgewählten Mechanismus unterstützt werden. Die **EncryptMessage (Schannel)-Funktion** verwendet den [*Sicherheitskontext,*](../secgloss/s-gly.md) auf den das Kontexthandle verweist. Einige Pakete verfügen nicht über Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen [*Integritätshash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Bei Verwendung des Schannel-SSP verschlüsselt diese Funktion Nachrichten mithilfe eines [*Sitzungsschlüssels,*](../secgloss/s-gly.md) der mit der Remotepartei ausgehandelt wird, die die Nachricht empfängt. Der Verschlüsselungsalgorithmus wird von der verwendeten [ [*Verschlüsselungssammlung*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) bestimmt.

> [!Note]  
> **EncryptMessage (Schannel)** und [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) können gleichzeitig von zwei verschiedenen Threads in einem einzelnen SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

| Wert                                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ \_ WRAP-OOB-DATEN \_**</dt> </dl> | Senden sie eine Schannel-Warnmeldung. In diesem Fall muss der *pMessage-Parameter* einen standardmäßigen SSL/TLS-Standardereigniscode mit zwei Byte enthalten. Dieser Wert wird nur vom Schannel-SSP unterstützt.<br/> Ab Windows Vista muss beispielsweise die Nachricht "server hello", die vom Server während der erneuten Authentifizierung gesendet wird, als TLS-Warnung verschlüsselt werden.<br/> |

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Typen kann vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird an Ort und Stelle verschlüsselt und überschreibt den ursprünglichen Inhalt der -Struktur.

Die Funktion verarbeitet keine Puffer mit dem SECBUFFER \_ READONLY-Attribut.

Die Länge der [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Nachricht enthält, darf nicht größer als **cbMaximumMessage** sein, die von der [**Funktion QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) (SECPKG \_ ATTR STREAM SIZES) abgerufen \_ \_ wird.

*MessageSeqNo* \[ In\]

Die Sequenznummer, die die Transportanwendung der Nachricht zugewiesen hat. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter 0 (null) sein.

Wenn Sie den Schannel-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ BUFFER \_ TOO \_ SMALL**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Eine ordnungsgemäß geschriebene Anwendung sollte diesen Fehler nicht erhalten.<br/>             |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt.<br/>                       |
| <dl> <dt>**SEC \_ E \_ INSUFFICIENT \_ MEMORY**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                           |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Ein ungültiges Kontexthandle wurde im *phContext-Parameter* angegeben.<br/>                                                                   |
| <dl> <dt>**SEC \_ E \_ INVALID \_ TOKEN**</dt> </dl>          | Es wurde kein \_ SECBUFFER-DATENTYPpuffer gefunden.<br/>                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**</dt> </dl>     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt.<br/> |

## <a name="remarks"></a>Hinweise

Die **Funktion EncryptMessage (Schannel)** verschlüsselt eine Nachricht basierend auf der Nachricht und dem [*Sitzungsschlüssel*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext.*](../secgloss/s-gly.md)

Wenn die Transportanwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenzerkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die Funktion diese Informationen mit der verschlüsselten Nachricht. Das Einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transportanwendung übergeben wird.

Bei Verwendung mit dem Schannel-SSP muss der *pMessage-Parameter* eine [**SecBufferDesc-Struktur**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) mit den folgenden Puffern enthalten.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| \_SECBUFFER-STREAMHEADER \_  | Wird intern verwendet. Keine Initialisierung erforderlich.                                                                        |
| SECBUFFER \_ DATA            | Enthält die zu verschlüsselnde [*Klartextnachricht.*](../secgloss/s-gly.md) |
| SECBUFFER \_ STREAM \_ TRAILER | Wird intern verwendet. Keine Initialisierung erforderlich.                                                                        |
| SECBUFFER \_ EMPTY           | Wird intern verwendet. Keine Initialisierung erforderlich. Die Größe kann 0 (null) sein.                                                      |

Wenn Sie den Schannel-SSP verwenden, bestimmen Sie die maximale Größe jedes Puffers, indem Sie die [**QueryContextAttributes (Schannel)-Funktion**](querycontextattributes--schannel.md) aufrufen und das SECPKG \_ ATTR \_ STREAM \_ SIZES-Attribut angeben. Diese Funktion gibt eine [**SecPkgContext \_ StreamSizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) zurück, deren Member die maximalen Größen für die Puffer header (**cbHeader** member), message (**cbMaximumMessage** member) und trailer (**cbTrailer** member) enthalten.

Um eine optimale Leistung zu erzielen, sollten die *pMessage-Strukturen* aus zusammenhängendem Speicher zugeordnet werden.

**Windows XP/2000:** Diese Funktion wurde auch als **SealMessage** bezeichnet. Anwendungen sollten jetzt nur **EncryptMessage (Schannel)** verwenden.

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
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
