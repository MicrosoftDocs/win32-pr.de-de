---
description: Verschlüsselt eine Meldung zur Bereitstellung des Datenschutzes mithilfe von Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Verschlüsseltmessage-Funktion (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217784"
---
# <a name="encryptmessage-kerberos-function"></a>Verschlüsseltmessage-Funktion (Kerberos)

Die Funktion " **verschlüsseltmessage" (Kerberos)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. Mithilfe von " **verschlüsseltmessage" (Kerberos)** kann eine Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden. Die Funktion " **verschlüsseltmessage" (Kerberos)** verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird. Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

> [!Note]  
> " **Verschlüsseltmessage (Kerberos)** " und " [**DecryptMessage" (Kerberos)**](decryptmessage--kerberos.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

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

*phcontext* \[ in\]
</dt> <dd>

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.

</dd> <dt>

vollständig verfügbar  \[ in\]
</dt> <dd>

Paket spezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.

Dieser Parameter kann das folgende Flag aufweisen.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Erzeugt einen Header oder Nachspann, aber verschlüsselt die Nachricht nicht.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr></tbody></table>

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ secbuffer-Daten aufweisen können \_ . Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.

Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.

Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.

Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .

</dd> <dt>

*Messageseqno* \[ in\]
</dt> <dd>

Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.                                                                                                                                                                 |
| <dl> <dt>**Sek. \_ E \_ Kontext \_ abgelaufen**</dt> </dl>        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.                                                                                               |
| <dl> <dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt> </dl> | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.                                                                                                         |
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>          | Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.                                                                                                                                                                                          |
| <dl> <dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt> </dl>     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt. |

## <a name="remarks"></a>Bemerkungen

Die Funktion " **verschlüsseltmessage" (Kerberos)** verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).

Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht. Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

| Puffertyp                           | BESCHREIBUNG                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Secbuffer \_ - \_ Streamheader<  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                       |
| secbuffer- \_ Daten            | Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht. |
| secbuffer- \_ streamnachspann \_ | Wird intern verwendet. Es ist keine Initialisierung erforderlich.                                                                        |
| secbuffer ist \_ leer.           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann NULL sein.                                                      |

Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet. Anwendungen sollten jetzt nur " **verschlüsseltmessage" (Kerberos)** verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\] |
| Header                   | SSPI. h (Include Security. h)               |
| Bibliothek                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Akzeptsecuritycontext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
