---
description: Verschlüsselt eine Nachricht, um Datenschutz zu gewährleisten.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: EncryptMessage(General)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6645d58b753503853dae7998982a32221d1f0d14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476286"
---
# <a name="encryptmessage-general-function"></a>EncryptMessage(General)-Funktion

Die **Funktion EncryptMessage (Allgemein)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. **EncryptMessage (Allgemein)** ermöglicht einer Anwendung die Auswahl zwischen [*kryptografischen Algorithmen,*](../secgloss/c-gly.md) die vom ausgewählten Mechanismus unterstützt werden. Die **EncryptMessage (General)-Funktion** verwendet den [*Sicherheitskontext,*](../secgloss/s-gly.md) auf den das Kontexthandle verweist. Einige Pakete verfügen nicht über Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen [*Integritätshash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Bei Verwendung des [*Digest-Sicherheitsunterstützungsanbieters*](../secgloss/s-gly.md) (SSP) ist diese Funktion nur als SASL-Mechanismus verfügbar.

Bei Verwendung des Schannel-SSP verschlüsselt diese Funktion Nachrichten mithilfe eines [*Sitzungsschlüssels,*](../secgloss/s-gly.md) der mit der Remotepartei ausgehandelt wird, die die Nachricht empfängt. Der Verschlüsselungsalgorithmus wird von der verwendeten [ [*Verschlüsselungssammlung*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) bestimmt.

> [!Note]  
> **EncryptMessage (Allgemein)** und [**DecryptMessage (Allgemein)**](decryptmessage--general.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

Informationen zur Verwendung dieser Funktion mit einem bestimmten SSP finden Sie in den folgenden Themen.

| Thema                                                            | BESCHREIBUNG                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (Digest)**](encryptmessage--digest.md)       | Verschlüsselt eine Nachricht, um Datenschutz mithilfe von Digest bereitzustellen.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Verschlüsselt eine Nachricht, um Mithilfe von Kerberos Datenschutz zu gewährleisten.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Verschlüsselt eine Nachricht, um Mithilfe von Negotiate Datenschutz zu gewährleisten. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Verschlüsselt eine Nachricht, um mit NTLM Datenschutz zu gewährleisten.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Verschlüsselt eine Nachricht, um Mithilfe von Schannel Datenschutz zu gewährleisten.  |

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

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden.

Dieser Parameter kann eines der folgenden Flags sein.


| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Erstellen Sie einen Header oder Nachspann, aber verschlüsseln Sie die Nachricht nicht.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl><dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt></dl> | Senden sie eine Schannel-Warnmeldung. In diesem Fall muss der <em>pMessage-Parameter</em> einen standardmäßigen SSL/TLS-Standardereigniscode mit zwei Byte enthalten. Dieser Wert wird nur vom Schannel-SSP unterstützt.<br /> | 


*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Typen kann vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird an Ort und Stelle verschlüsselt und überschreibt den ursprünglichen Inhalt der -Struktur.

Die Funktion verarbeitet keine Puffer mit dem SECBUFFER \_ READONLY-Attribut.

Die Länge der [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Nachricht enthält, darf nicht größer als **cbMaximumMessage** sein, die von der [**Funktion QueryContextAttributes (General)**](querycontextattributes--general.md) (SECPKG \_ ATTR STREAM SIZES) abgerufen \_ \_ wird.

Bei Verwendung des Digest-SSP muss ein zweiter Puffer vom Typ SECBUFFER \_ PADDING oder SEC \_ BUFFER DATA \_ vorhanden sein, um [*Signaturinformationen*](../secgloss/d-gly.md#_security_digital_signature_gly) zu speichern. Um die Größe des Ausgabepuffers abzurufen, rufen Sie die [**QueryContextAttributes (General)-Funktion**](querycontextattributes--general.md) auf, und geben Sie SECPKG \_ ATTR \_ SIZES an. Die Funktion gibt eine [**SecPkgContext \_ Sizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **Membern cbMaxSignature** und **cbBlockSize.**

Anwendungen, die SSL nicht verwenden, müssen einen [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ SECBUFFER \_ PADDING bereitstellen.

*MessageSeqNo* \[ In\]

Die Sequenznummer, die die Transportanwendung der Nachricht zugewiesen hat. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter 0 (null) sein.

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenznummerierung intern.

Wenn Sie den Schannel-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                         | Beschreibung                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ BUFFER \_ TOO \_ SMALL**      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                                                          |
| **SEC \_ E \_ CONTEXT \_ EXPIRED**        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Eine ordnungsgemäß geschriebene Anwendung sollte diesen Fehler nicht erhalten.                                        |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt.                                                                       |
| **SEC \_ E \_ INSUFFICIENT \_ MEMORY**    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                                                                      |
| **SEC \_ E \_ INVALID \_ HANDLE**         | Im *phContext-Parameter* wurde ein ungültiges Kontexthandle angegeben.                                                                                              |
| **SEC \_ E \_ INVALID \_ TOKEN**          | Es wurde kein \_ SECBUFFER-DATENTYPpuffer gefunden.                                                                                                                                   |
| **SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt. |

## <a name="remarks"></a>Hinweise

Die **EncryptMessage (General)-Funktion** verschlüsselt eine Nachricht basierend auf der Nachricht und dem [*Sitzungsschlüssel*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext.*](../secgloss/s-gly.md)

Wenn die Transportanwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenzerkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die Funktion diese Informationen mit der verschlüsselten Nachricht. Das Einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transportanwendung übergeben wird.

Wenn Sie den Digest-SSP verwenden, rufen Sie die Größe des Ausgabepuffers ab, indem Sie die [**QueryContextAttributes (General)-Funktion**](querycontextattributes--general.md) aufrufen und SECPKG \_ ATTR \_ SIZES angeben. Die Funktion gibt eine [**SecPkgContext \_ Sizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **Membern cbMaxSignature** und **cbBlockSize.**

Bei Verwendung mit dem Schannel-SSP muss der *pMessage-Parameter* eine [**SecBufferDesc-Struktur**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) mit den folgenden Puffern enthalten.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                | BESCHREIBUNG                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_SECBUFFER-STREAMHEADER \_  | Wird intern verwendet. Keine Initialisierung erforderlich.                                                |
| SECBUFFER \_ DATA            | Enthält die [*zu verschlüsselnde Klartextnachricht.*](../secgloss/s-gly.md) |
| SECBUFFER \_ STREAM \_ TRAILER | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                |
| SECBUFFER \_ EMPTY           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann 0 (null) sein.                              |

Wenn Sie den Schannel-SSP verwenden, bestimmen Sie die maximale Größe der einzelnen Puffer, indem Sie die [**QueryContextAttributes (General)-Funktion**](querycontextattributes--general.md) aufrufen und das SECPKG \_ ATTR \_ STREAM \_ SIZES-Attribut angeben. Diese Funktion gibt eine [**SecPkgContext \_ StreamSizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) zurück, deren Member die maximalen Größen für die Puffer header (**cbHeader** member), message (**cbMaximumMessage** member) und trailer **(cbTrailer** member) enthalten.

Um eine optimale Leistung zu erzielen, sollten *die pMessage-Strukturen* aus dem zusammenhängenden Speicher zugeordnet werden.

**Windows XP/2000:** Diese Funktion wurde auch als **SealMessage bezeichnet.** Anwendungen sollten jetzt **nur EncryptMessage (Allgemein)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\]                                                            |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\]                                                   |
| Header                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |
| Bibliothek                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Weitere Informationen

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Allgemein)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (Allgemein)**](decryptmessage--general.md)
- [**InitializeSecurityContext (Allgemein)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (Allgemein)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
