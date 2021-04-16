---
description: Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von aushandeln bereitzustellen.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: Verschlüsselungsmessage (aushandeln)-Funktion
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 037866088f58fa1d70939b84062161a6e4f610b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348099"
---
# <a name="encryptmessage-negotiate-function"></a>Verschlüsselungsmessage (aushandeln)-Funktion

Die Funktion " **verschlüsseltmessage" (aushandeln)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. Mit **verschlüsselungsmessage (aushandeln)** kann die Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden. Die Funktion " **verschlüsseltmessage (aushandeln)** " verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird. Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

> [!Note]  
> **Verschlüsselungsmessage (aushandeln)** und [**DecryptMessage (aushandeln)**](decryptmessage--negotiate.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phcontext* \[ in \] einem Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.

vollständig verfügbar  \[ in \] Paket spezifischen Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.

Dieser Parameter kann das folgende Flag aufweisen.

| Wert                  | Bedeutung                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Erzeugt einen Header oder Nachspann, aber verschlüsselt die Nachricht nicht. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.

*pMessage* \[ in \] einen Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ secbuffer-Daten aufweisen können \_ . Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.

Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.

Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (Aushandlungs)**](querycontextattributes--negotiate.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.

Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .

*Messageseqno* \[ in \] der Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Sekunde \_ E \_ Puffer \_ zu \_ klein**      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                   |
| **Sek. \_ E \_ Kontext \_ abgelaufen**        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden. |
| **s \_ E \_ \_ Kryptografiesystem \_ ungültig** | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.                                |
| **SEK \_ b \_ nicht genügend Arbeits \_ Speicher**    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                               |
| **s \_ E \_ ungültiges \_ handle**         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.                                                       |
| **s \_ E \_ ungültiges \_ Token**          | Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.                                                                                            |
| **Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt.             |

## <a name="remarks"></a>Bemerkungen

Die Funktion " **verschlüsseltmessage (aushandeln)** " verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).

Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht. Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| secbuffer \_ - \_ Streamheader  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                |
| secbuffer- \_ Daten            | Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht. |
| secbuffer- \_ streamnachspann \_ | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                |
| secbuffer ist \_ leer.           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann NULL sein.                              |

Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet. Anwendungen sollten jetzt nur " **verschlüsseltmessage (aushandeln)** " verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]                |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\]       |
| Header                   | SSPI. h (Include Security. h)                     |
| Bibliothek                  | Secur32. lib                                     |
| DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Akzeptsecuritycontext (aushandeln)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (aushandeln)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (aushandeln)**](querycontextattributes--negotiate.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
