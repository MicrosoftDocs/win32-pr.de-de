---
description: Entschlüsselt eine Nachricht mithilfe von Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage-Funktion (SChannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750041"
---
# <a name="decryptmessage-schannel-function"></a>DecryptMessage-Funktion (SChannel)

Die Funktion **DecryptMessage (SChannel)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln Nachrichten nicht, sondern führen einen Integritäts [*Hash*](../secgloss/h-gly.md)aus und überprüfen Sie.


Diese Funktion wird auch mit dem SChannel- [*Security Support Provider*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) (SSP) verwendet, um eine Anforderung von einem Nachrichten Absender für eine erneute Aushandlung (Wiederholung) der Verbindungs Attribute oder für das Herunterfahren der Verbindung zu signalisieren.

> [!Note]  
> " [**Verschlüsseltmessage" (SChannel)**](encryptmessage--schannel.md) und " **DecryptMessage" (SChannel)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.


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


Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) , der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen. Eine dieser Typen kann vom Typ "secbuffer \_ Data" sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird direkt entschlüsselt und überschreibt den ursprünglichen Inhalt Ihres Puffers.

Wenn der Schannel-SSP mit Kontexten verwendet wird, die nicht verbindungsorientiert sind, muss die Struktur bei der Eingabe vier [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen enthalten. Genau ein Puffer muss den Typ "secbuffer \_ Data" aufweisen und eine verschlüsselte Nachricht enthalten, die an Ort und Stelle entschlüsselt wird. Die restlichen Puffer werden für die Ausgabe verwendet und müssen den Typ "secbuffer Empty" aufweisen \_ . Bei Verbindungs orientierten Kontexten muss ein secbuffer \_ -Datentyp Puffer angegeben werden, wie für nicht Verbindungs orientierte Kontexte angegeben. Darüber hinaus muss auch ein zweiter Typ eines secbuffer- \_ Tokentyps, der ein Sicherheits Token enthält, bereitgestellt werden.

*Messageseqno* \[ in\]

Die Sequenznummer, die von der Transport Anwendung erwartet wird, falls vorhanden. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter auf 0 (null) festgelegt werden.

Bei Verwendung des Schannel-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

*pfqop* \[ vorgenommen\]

Ein Zeiger auf eine Variable vom Typ **ulong** , die Paket spezifische Flags empfängt, die die Qualität des Schutzes angeben.

Wenn der Schannel SSP verwendet wird, wird dieser Parameter nicht verwendet und sollte auf **null** festgelegt werden.

Dieser Parameter kann das folgende Flag aufweisen.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder ein Nachspann erzeugt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat denselben Wert und dieselbe Bedeutung.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, wird einer der folgenden Fehlercodes zurückgegeben.

| Rückgabecode                     | Beschreibung                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ ungültiges \_ handle**     | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben. Wird mit dem Schannel SSP verwendet.     |
| **s \_ E \_ ungültiges \_ Token**      | Die Puffer weisen den falschen Typ auf, oder es wurde kein Puffer vom Typ "secbuffer \_ Data" gefunden. Wird mit dem Schannel SSP verwendet.  |
| **Sek. \_ E- \_ Nachricht \_ geändert**    | Die Nachricht wurde geändert. Wird mit dem Schannel SSP verwendet.                                                      |
| **Sek. \_ E \_ außerhalb \_ der \_ Reihenfolge**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                          |
| **Sek., \_ \_ Kontext \_ abgelaufen**    | Der Absender der Nachricht hat die Verbindung nicht mehr hergestellt und hat ein Herunterfahren initiiert. Informationen zum initiieren oder erkennen eines herunter Fahrens finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md). Wird mit dem Schannel SSP verwendet. |
| **Sekunde, die \_ ich erneut \_ verhandate**         | Die Remote Partei benötigt eine neue Hand Shake Sequenz, oder die Anwendung hat gerade ein Herunterfahren initiiert. Kehren Sie zur Aushandlungs Schleife zurück, und nennen Sie " [**Accept-SecurityContext" (SChannel)**](acceptsecuritycontext--schannel.md) oder " [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)", und übergeben Sie SECBUFFER_EXTRA von DecryptMessage () zurückgegeben. Die Neuverhandlung wird für den SChannel-Kernel Modus nicht unterstützt. Der Aufrufer sollte entweder diesen Rückgabewert ignorieren oder die Verbindung beenden. Wenn der Wert ignoriert wird, kann die Verbindung entweder vom Client oder vom Server beendet werden. |


## <a name="remarks"></a>Bemerkungen

Manchmal liest eine Anwendung Daten von der Remote Partei, versucht Sie, Sie mithilfe von **DecryptMessage (SChannel)** zu entschlüsseln, und erkennt, dass **DecryptMessage (SChannel)** erfolgreich war, aber die Ausgabepuffer leer sind. Dies ist das normale Verhalten, und Anwendungen müssen damit umgehen können.

Wenn Sie Schannel SSP verwenden, gibt die Funktion [**DecryptMessage (allgemein)**](decryptmessage--general.md) den Wert Sekunde zurück, den der \_ \_ Kontext \_ abgelaufen ist, wenn der Absender der Nachricht die Verbindung beendet hat. Informationen zum initiieren oder erkennen eines herunter Fahrens finden Sie unter Herunterfahren [einer SChannel-Verbindung](shutting-down-an-schannel-connection.md).

Wenn Sie TLS 1,0 verwenden, müssen Sie diese Funktion möglicherweise mehrmals aufzurufen, indem Sie den Eingabepuffer jedes Aufrufes so anpassen, dass eine ganze Nachricht entschlüsselt wird.


Die Funktion **DecryptMessage (SChannel)** gibt Sekunde zurück \_ , die ich erneut aushandeln möchte \_ , wenn der Absender der Nachricht die Verbindung erneut aushandeln möchte ([*Sicherheitskontext*](../secgloss/s-gly.md)). Eine Anwendung verarbeitet eine angeforderte Neuverhandlung durch Aufrufen von " [**Accept-SecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) " (serverseitig) oder " [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) " (Client seitig) und "Pass SECBUFFER_EXTRA von DecryptMessage ()" zurückgegeben. Nachdem dieser anfängliche-Befehl einen Wert zurückgegeben hat, fahren Sie so fort, als ob die Anwendung eine neue Verbindung erstellt hat. Weitere Informationen finden Sie unter [Erstellen eines SChannel-Sicherheits Kontexts](creating-an-schannel-security-context.md).


## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP \[ -Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003 \[ -Desktop-Apps\] |
| Header                   | SSPI. h (Include Security. h)               |
| Bibliothek                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**Verschlüsselungs Meldung (SChannel)**](encryptmessage--schannel.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
