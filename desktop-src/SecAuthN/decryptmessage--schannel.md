---
description: Entschlüsselt eine Nachricht mithilfe von Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage-Funktion (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: feec97f9e989270d812458cd61ff34132d118d192108c3f2372b192f2e383464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008478"
---
# <a name="decryptmessage-schannel-function"></a>DecryptMessage-Funktion (Schannel)

Die **Funktion DecryptMessage (Schannel)** entschlüsselt eine Nachricht. Einige Pakete verschlüsseln und entschlüsseln nachrichten nicht, sondern führen stattdessen einen Integritätshash aus und [*überprüfen diesen.*](../secgloss/h-gly.md)


Diese Funktion wird auch mit dem Schannel-Sicherheitssupportanbieter (Security [*Support Provider,*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) SSP) verwendet, um eine Anforderung von einem Nachrichtensender für eine Neuverhandlung (Wiederholen) der Verbindungsattribute oder für das Herunterfahren der Verbindung zu signalisieren.

> [!Note]  
> [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) und **DecryptMessage (Schannel)** können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.


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

*phContext* \[ In\]


Ein Handle für den [*Sicherheitskontext,*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) der zum Entschlüsseln der Nachricht verwendet werden soll.

*pMessage* \[ in, out\]

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Eine dieser Typen kann vom Typ SECBUFFER \_ DATA sein. Dieser Puffer enthält die verschlüsselte Nachricht. Die verschlüsselte Nachricht wird an Ort und Stelle entschlüsselt und überschreiben den ursprünglichen Inhalt des Puffers.

Wenn Sie den Schannel-SSP mit Kontexten verwenden, die nicht verbindungsorientiert sind, muss die Struktur bei der Eingabe vier [**SecBuffer-Strukturen**](/windows/win32/api/sspi/ns-sspi-secbuffer) enthalten. Genau ein Puffer muss vom Typ SECBUFFER DATA sein und eine verschlüsselte Nachricht \_ enthalten, die an Ort und Stelle entschlüsselt wird. Die verbleibenden Puffer werden für die Ausgabe verwendet und müssen vom Typ SECBUFFER \_ EMPTY sein. Für verbindungsorientierte Kontexte muss ein SECBUFFER DATA-Typpuffer bereitgestellt werden, wie für \_ nichtconnectionorientierte Kontexte angegeben. Darüber hinaus muss auch ein zweiter SECBUFFER TOKEN-Typpuffer bereitgestellt werden, der ein \_ Sicherheitstoken enthält.

*MessageSeqNo* \[ In\]

Die sequenznummer, die von der Transportanwendung erwartet wird, sofern eine davon der Fall ist. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter auf 0 (null) festgelegt werden.

Bei Verwendung des Schannel-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Schannel-SSP verwendet keine Sequenznummern.

*pfQOP* \[ out\]

Ein Zeiger auf eine Variable vom Typ **ULONG,** die paketspezifische Flags empfängt, die die Qualität des Schutzes angeben.

Bei Verwendung des Schannel-SSP wird dieser Parameter nicht verwendet und sollte auf NULL festgelegt **werden.**

Dieser Parameter kann das folgende Flag sein.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Die Nachricht wurde nicht verschlüsselt, aber es wurde ein Header oder Nachspann erstellt.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT hat den gleichen Wert und dieselbe Bedeutung.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion überprüft, ob die Nachricht in der richtigen Reihenfolge empfangen wurde, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion die Nachricht nicht entschlüsseln kann, gibt sie einen der folgenden Fehlercodes zurück.

| Rückgabecode                     | Beschreibung                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **SEC \_ E \_ UNGÜLTIGES \_ HANDLE**     | Im *phContext-Parameter* wurde ein ungültiges Kontexthand handle angegeben. Wird mit dem Schannel-SSP verwendet.     |
| **SEC \_ E \_ UNGÜLTIGES \_ TOKEN**      | Die Puffer sind vom falschen Typ, oder es wurde kein Puffer vom Typ SECBUFFER \_ DATA gefunden. Wird mit dem Schannel-SSP verwendet.  |
| **SEC \_ E \_ MESSAGE \_ ALTERED**    | Die Nachricht wurde geändert. Wird mit dem Schannel-SSP verwendet.                                                      |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | Die Nachricht wurde nicht in der richtigen Reihenfolge empfangen.                                                          |
| **SEC \_ I \_ CONTEXT \_ EXPIRED**    | Der Absender der Nachricht hat die Verbindung beendet und das Herunterfahren initiiert. Informationen zum Initiieren oder Erkennen eines Herunterfahrens finden Sie unter [Herunterfahren einer Schannel-Verbindung.](shutting-down-an-schannel-connection.md) Wird mit dem Schannel-SSP verwendet. |
| **SEC \_ I \_ RENEGOTIATE**         | Die Remoteparty erfordert eine neue Handshakesequenz, oder die Anwendung hat gerade ein Herunterfahren initiiert. Kehren Sie zur Aushandlungsschleife zurück, und rufen Sie [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) oder [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)auf, und übergeben Sie SECBUFFER_EXTRA DecryptMessage(). Die Neuverhandlung wird für den Schannel-Kernelmodus nicht unterstützt. Der Aufrufer sollte diesen Rückgabewert ignorieren oder die Verbindung herunterfahren. Wenn der Wert ignoriert wird, wird die Verbindung möglicherweise entweder vom Client oder vom Server heruntergefahren. |


## <a name="remarks"></a>Hinweise

Manchmal liest eine Anwendung Daten von der Remote-Partei, versucht, sie mithilfe von **DecryptMessage (Schannel)** zu entschlüsseln, und festgestellt, dass **DecryptMessage (Schannel)** erfolgreich war, die Ausgabepuffer jedoch leer sind. Dies ist ein normales Verhalten, und Anwendungen müssen damit umgehen können.

Wenn Sie den Schannel-SSP verwenden, gibt die [**Funktion DecryptMessage (General)**](decryptmessage--general.md) SEC I CONTEXT EXPIRED zurück, wenn der Absender der Nachricht \_ die Verbindung \_ \_ heruntergefahren hat. Informationen zum Initiieren oder Erkennen eines Herunterfahrens finden Sie unter [Herunterfahren einer Schannel-Verbindung.](shutting-down-an-schannel-connection.md)

Wenn Sie TLS 1.0 verwenden, müssen Sie diese Funktion möglicherweise mehrmals aufrufen und dabei den Eingabepuffer bei jedem Aufruf anpassen, um eine ganze Nachricht zu entschlüsseln.


Die **Funktion DecryptMessage (Schannel)** gibt SEC \_ I RENEGOTIATE zurück, wenn der Absender der Nachricht die Verbindung erneut aushandeln möchte \_ [*(Sicherheitskontext*](../secgloss/s-gly.md)). Eine Anwendung verarbeitet eine angeforderte Neuverhandlung, indem sie [**AcceptSecurityContext (Schannel) (serverseitig)**](acceptsecuritycontext--schannel.md) oder [**InitializeSecurityContext (Schannel) (clientseitig)**](initializesecuritycontext--schannel.md) aufruft und SECBUFFER_EXTRA von DecryptMessage() zurückgegebene Übergeben. Nachdem dieser erste Aufruf einen Wert zurückgegeben hat, fahren Sie so fort, als ob Ihre Anwendung eine neue Verbindung erstellt hat. Weitere Informationen finden Sie unter [Erstellen eines Schannel-Sicherheitskontexts.](creating-an-schannel-security-context.md)


## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows Nur \[ XP-Desktop-Apps\]          |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2003-Desktop-Apps\] |
| Header                   | Sspi.h (einschließlich Security.h)               |
| Bibliothek                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Siehe auch

- [SSPI-Funktionen](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
