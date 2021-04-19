---
description: Verschlüsselt eine Nachricht, um Datenschutz bereitzustellen.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Verschlüsseltmessage (allgemein)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3c661f5f529700db19683966783c1aa0793e376b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343251"
---
# <a name="encryptmessage-general-function"></a>Verschlüsseltmessage (allgemein)-Funktion

Die Funktion " **verschlüsseltmessage (allgemein)** " verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. Mit **verschlüsselungsmessage (allgemein)** kann eine Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden. Die Funktion " **verschlüsseltmessage (allgemein)** " verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird. Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Wenn die Digest- [*Security Support Provider*](../secgloss/s-gly.md) (SSP) verwendet wird, ist diese Funktion nur als SASL-Mechanismus verfügbar.

Bei Verwendung des Schannel-SSP verschlüsselt diese Funktion Nachrichten mithilfe eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) , der mit dem Remote Anbieter ausgehandelt wird, der die Nachricht empfängt. Der Verschlüsselungsalgorithmus wird von der verwendeten Verschlüsselungs [ [](../secgloss/c-gly.md) Sammlung]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) bestimmt.

> [!Note]  
> **Verschlüsselungsmessage (allgemein)** und [**DecryptMessage (allgemein)**](decryptmessage--general.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

Informationen zur Verwendung dieser Funktion mit einem bestimmten SSP finden Sie in den folgenden Themen.

| Thema                                                            | BESCHREIBUNG                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**Verschlüsselungs Meldung (Digest)**](encryptmessage--digest.md)       | Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von Digest bereitzustellen.    |
| [**Verschlüsselungs Meldung (Kerberos)**](encryptmessage--kerberos.md)   | Verschlüsselt eine Meldung zur Bereitstellung des Datenschutzes mithilfe von Kerberos.  |
| [**Verschlüsselungsnachricht (aushandeln)**](encryptmessage--negotiate.md) | Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von aushandeln bereitzustellen. |
| [**Verschlüsselungs Meldung (NTLM)**](encryptmessage--ntlm.md)           | Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von NTLM bereitzustellen.      |
| [**Verschlüsselungs Meldung (SChannel)**](encryptmessage--schannel.md)   | Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von SChannel bereitzustellen.  |

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

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden.

Dieser Parameter kann eines der folgenden Flags sein.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Erzeugt einen Header oder Nachspann, aber verschlüsselt die Nachricht nicht.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr><tr class="even"><td><span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt> </dl></td><td>Eine SChannel-Warnmeldung senden. In diesem Fall muss der <em>pMessage</em> -Parameter einen standardmäßigen zwei-Byte-SSL/TLS-Ereignis Code enthalten. Dieser Wert wird nur vom Schannel SSP unterstützt.<br/></td></tr></tbody></table>

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eines dieser Typen kann vom Typ "secbuffer \_ Data" sein. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.

Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.

Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (General)**](querycontextattributes--general.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.

Bei der Verwendung des Digest-SSP muss ein zweiter Puffer vom Typ "secbuffer \_ Padding" oder "sec"-Puffer Daten vorhanden sein, \_ um die \_ [*Signatur*](../secgloss/d-gly.md#_security_digital_signature_gly) Informationen zu speichern. Um die Größe des Ausgabepuffers abzurufen, nennen Sie die Funktion [**QueryContextAttributes (allgemein)**](querycontextattributes--general.md) , und geben Sie die Größe der secpkg- \_ attr an \_ . Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.

Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .

*Messageseqno* \[ in\]

Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenz Nummerierung intern.

Bei Verwendung des Schannel-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sekunde \_ E \_ Puffer \_ zu \_ klein**      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                                                          |
| **Sek. \_ E \_ Kontext \_ abgelaufen**        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.                                        |
| **s \_ E \_ \_ Kryptografiesystem \_ ungültig** | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.                                                                       |
| **SEK \_ b \_ nicht genügend Arbeits \_ Speicher**    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                                                                      |
| **s \_ E \_ ungültiges \_ handle**         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.                                                                                              |
| **s \_ E \_ ungültiges \_ Token**          | Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.                                                                                                                                   |
| **Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt. |

## <a name="remarks"></a>Bemerkungen

Die Funktion " **verschlüsseltmessage (allgemein)** " verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).

Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht. Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.

Wenn Sie den Digest-SSP verwenden, rufen Sie die Größe des Ausgabepuffers ab, indem Sie die Funktion [**QueryContextAttributes (allgemein)**](querycontextattributes--general.md) aufrufen und die Größe der secpkg- \_ attr angeben \_ . Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.

Bei Verwendung mit dem Schannel SSP muss der *pMessage* -Parameter eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur mit den folgenden Puffern enthalten.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| secbuffer \_ - \_ Streamheader  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                |
| secbuffer- \_ Daten            | Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht. |
| secbuffer- \_ streamnachspann \_ | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                |
| secbuffer ist \_ leer.           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann NULL sein.                              |

Wenn Sie Schannel SSP verwenden, bestimmen Sie die maximale Größe der einzelnen Puffer, indem Sie die Funktion [**QueryContextAttributes (allgemein)**](querycontextattributes--general.md) aufrufen und das Attribut secpkg \_ attr \_ Stream \_ sizes angeben. Diese Funktion gibt eine [**secpkgcontext- \_ streamsizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) -Struktur zurück, deren Member die maximale Größe für die Header (**cbheader** -Member), Message (**cbmaximummess** -Member) und Nachspann (**cbtrailer** -Member) enthalten.

Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.

**Windows XP/2000:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet. Anwendungen sollten jetzt nur " **verschlüsseltmessage (allgemein)** " verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]                                                            |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\]                                                   |
| Header                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Akzeptsecuritycontext (allgemein)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (allgemein)**](decryptmessage--general.md)
- [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (allgemein)**](querycontextattributes--general.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
