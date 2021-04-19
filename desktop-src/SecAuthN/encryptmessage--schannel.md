---
description: Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von SChannel bereitzustellen.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Verschlüsseltmessage-Funktion (SChannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3075b2fe7e5b4167a5a8527a16009282b2fca1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355347"
---
# <a name="encryptmessage-schannel-function"></a>Verschlüsseltmessage-Funktion (SChannel)

Die Funktion " **verschlüsseltmessage" (SChannel)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. Mit " **verschlüsseltmessage" (SChannel)** kann eine Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) wählen, die vom ausgewählten Mechanismus unterstützt werden. Die " **verschlüsseltmessage"-Funktion (SChannel)** verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird. Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Bei Verwendung des Schannel-SSP verschlüsselt diese Funktion Nachrichten mithilfe eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) , der mit dem Remote Anbieter ausgehandelt wird, der die Nachricht empfängt. Der Verschlüsselungsalgorithmus wird von der verwendeten Verschlüsselungs [ [](../secgloss/c-gly.md) Sammlung]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) bestimmt.

> [!Note]  
> " **Verschlüsseltmessage" (SChannel)** und " [**DecryptMessage" (SChannel)**](decryptmessage--schannel.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phcontext* \[ in\]

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.

vollständig verfügbar  \[ in\]

Paket spezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.

Dieser Parameter kann das folgende Flag aufweisen.

| Wert                                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**secqop \_ Wrap \_ OOB- \_ Daten**</dt> </dl> | Eine SChannel-Warnmeldung senden. In diesem Fall muss der *pMessage* -Parameter einen standardmäßigen zwei-Byte-SSL/TLS-Ereignis Code enthalten. Dieser Wert wird nur vom Schannel SSP unterstützt.<br/> Beispielsweise muss ab Windows Vista die vom Server während des Authentifizierungs Protokolls gesendete "Server-Hello"-Meldung als TLS-Warnung verschlüsselt werden.<br/> |

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eines dieser Typen kann vom Typ "secbuffer \_ Data" sein. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.

Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.

Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes-Funktion (SChannel)**](querycontextattributes--schannel.md) (secpkg \_ attr \_ Stream \_ sizes) abgerufen wird.

*Messageseqno* \[ in\]

Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.

Bei Verwendung des Schannel-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                               |
| <dl> <dt>**Sek. \_ E \_ Kontext \_ abgelaufen**</dt> </dl>        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.<br/>             |
| <dl> <dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt> </dl> | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.<br/>                       |
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                           |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.<br/>                                                                   |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>          | Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.<br/>                                                                                                        |
| <dl> <dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt> </dl>     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt.<br/> |

## <a name="remarks"></a>Bemerkungen

Die Funktion " **verschlüsseltmessage" (SChannel)** verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).

Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht. Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.

Bei Verwendung mit dem Schannel SSP muss der *pMessage* -Parameter eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur mit den folgenden Puffern enthalten.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| secbuffer \_ - \_ Streamheader  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                        |
| secbuffer- \_ Daten            | Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht. |
| secbuffer- \_ streamnachspann \_ | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                        |
| secbuffer ist \_ leer.           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann NULL sein.                                                      |

Wenn Sie Schannel SSP verwenden, bestimmen Sie die maximale Größe der einzelnen Puffer, indem Sie die [**QueryContextAttributes-Funktion (SChannel)**](querycontextattributes--schannel.md) aufrufen und das Attribut secpkg \_ attr \_ Stream \_ sizes angeben. Diese Funktion gibt eine [**secpkgcontext- \_ streamsizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) -Struktur zurück, deren Member die maximale Größe für die Header (**cbheader** -Member), Message (**cbmaximummess** -Member) und Nachspann (**cbtrailer** -Member) enthalten.

Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.

**Windows XP/2000:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet. Anwendungen sollten jetzt nur " **verschlüsseltmessage" (SChannel)** verwenden.

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
- [**Akzeptsecuritycontext (SChannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (SChannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (SChannel)**](querycontextattributes--schannel.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
