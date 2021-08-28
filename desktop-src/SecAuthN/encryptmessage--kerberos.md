---
description: Verschlüsselt eine Nachricht, um Datenschutz mithilfe von Kerberos bereitzustellen.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: EncryptMessage-Funktion (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 89c6504fe8518e1c43d155ebce638dec1acfeb80
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476216"
---
# <a name="encryptmessage-kerberos-function"></a>EncryptMessage-Funktion (Kerberos)

Die **EncryptMessage-Funktion (Kerberos)** verschlüsselt eine Nachricht, um Datenschutz [*zu gewährleisten.*](../secgloss/p-gly.md) **EncryptMessage (Kerberos)** ermöglicht es einer Anwendung, zwischen kryptografischen Algorithmen zu [*wählen,*](../secgloss/c-gly.md) die vom ausgewählten Mechanismus unterstützt werden. Die **EncryptMessage(Kerberos)-Funktion** verwendet den [*Sicherheitskontext,*](../secgloss/s-gly.md) auf den das Kontexthand handle verweist. Einige Pakete verfügen nicht über Nachrichten, die verschlüsselt [](../secgloss/h-gly.md) oder entschlüsselt werden sollen, sondern bieten einen Integritätshash, der überprüft werden kann.

> [!Note]  
> **EncryptMessage (Kerberos)** und [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

<dl> <dt>

*phContext* \[ In\]
</dt> <dd>

Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md) der zum Verschlüsseln der Nachricht verwendet werden soll.

</dd> <dt>

*fQOP* \[ In\]
</dt> <dd>

Paketspezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket kann*](../secgloss/s-gly.md) diesen Parameter verwenden, um die Auswahl kryptografischer [*Algorithmen zu aktivieren.*](../secgloss/c-gly.md)

Dieser Parameter kann das folgende Flag sein.


| Wert | Bedeutung | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Erstellen Sie einen Header oder Nachspann, verschlüsseln Sie die Nachricht jedoch nicht.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br /> | 


</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die vom Typ SECBUFFER DATA sein \_ können. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird an Ort und Stelle verschlüsselt und überschreiben den ursprünglichen Inhalt der -Struktur.

Die Funktion verarbeiten keine Puffer mit dem SECBUFFER \_ READONLY-Attribut.

Die Länge der [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Nachricht enthält, darf nicht größer als **cbMaximumMessage** sein, die von der [**QueryContextAttributes (Kerberos)-Funktion**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES) abgerufen wird.

Anwendungen, die kein SSL verwenden, müssen [**einen SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ SECBUFFER \_ PADDING zur Verfügung stellen.

</dd> <dt>

*MessageSeqNo* \[ In\]
</dt> <dd>

Die Sequenznummer, die die Transportanwendung der Nachricht zugewiesen hat. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ BUFFER \_ TOO \_ SMALL**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | Die Anwendung bezieht sich auf einen Kontext, der bereits geschlossen wurde. Eine ordnungsgemäß geschriebene Anwendung sollte diesen Fehler nicht erhalten.                                                                                               |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | Die [*für den*](../secgloss/c-gly.md) Sicherheitskontext ausgewählte Verschlüsselung wird nicht unterstützt. [](../secgloss/s-gly.md)                                                                                                         |
| <dl> <dt>**\_S.E \_ NICHT GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abschließen zu können.                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ HANDLE**</dt> </dl>         | Im *phContext-Parameter* wurde ein ungültiges Kontexthand handle angegeben.                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ UNGÜLTIGES \_ TOKEN**</dt> </dl>          | Es wurde kein \_ SECBUFFER-DATENTYPpuffer gefunden.                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP \_ NOT \_ SUPPORTED**</dt> </dl>     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext unterstützt.*](../secgloss/s-gly.md) |

## <a name="remarks"></a>Hinweise

Die **EncryptMessage-Funktion (Kerberos)** verschlüsselt eine Nachricht basierend auf der Nachricht und dem Sitzungsschlüssel [*aus*](../secgloss/s-gly.md) einem [*Sicherheitskontext.*](../secgloss/s-gly.md)

Wenn die Transportanwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenzerkennung erstellt hat und der Aufrufer eine Sequenznummer enthält, schließt die Funktion diese Informationen in die verschlüsselte Nachricht ein. Das Einfügen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transportanwendung übergeben wurde.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                           | BESCHREIBUNG                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ SECBUFFER-STREAMHEADER<  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                       |
| \_SECBUFFER-DATEN            | Enthält die [*zu verschlüsselnde Klartextnachricht.*](../secgloss/s-gly.md) |
| SECBUFFER \_ STREAM \_ TRAILER | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                        |
| SECBUFFER \_ EMPTY           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann 0 (null) sein.                                                      |

Um eine optimale Leistung zu erzielen, sollten *die pMessage-Strukturen* aus dem zusammenhängenden Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als **SealMessage bezeichnet.** Anwendungen sollten jetzt nur **noch EncryptMessage (Kerberos)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (einschließlich Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
