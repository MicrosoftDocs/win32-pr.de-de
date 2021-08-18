---
description: Verschlüsselt eine Nachricht, um Datenschutz mithilfe von Digest bereitzustellen.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: EncryptMessage(Digest)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: af16238ca58449c286edd9eabb88d7bc9a3f7fa781fac360863fdd52f7296833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008428"
---
# <a name="encryptmessage-digest-function"></a>EncryptMessage-Funktion (Digest)

Die **Funktion EncryptMessage (Digest)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. **EncryptMessage (Digest)** ermöglicht der Anwendung die Auswahl zwischen [*kryptografischen Algorithmen,*](../secgloss/c-gly.md) die vom ausgewählten Mechanismus unterstützt werden. Die **EncryptMessage (Digest)-Funktion** verwendet den [*Sicherheitskontext,*](../secgloss/s-gly.md) auf den das Kontexthandle verweist. Einige Pakete verfügen nicht über Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen [*Integritätshash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Diese Funktion ist nur als SASL-Mechanismus verfügbar.

> [!Note]  
> **EncryptMessage (Digest)** und [**DecryptMessage (Digest)**](decryptmessage--digest.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext [*(Security Support Provider Interface)*](../secgloss/s-gly.md) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehr als ein Thread verschlüsselt wird oder mehrere Threads entschlüsselt werden, sollte jeder Thread einen eindeutigen Kontext erhalten.

 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
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

Paketspezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl [*kryptografischer Algorithmen*](../secgloss/c-gly.md)zu aktivieren.

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**SecBufferDesc-Struktur.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Bei der Eingabe verweist die -Struktur auf eine oder mehrere [**SecBuffer-Strukturen,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die vom Typ SECBUFFER DATA sein \_ können. Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird an Ort und Stelle verschlüsselt und überschreibt den ursprünglichen Inhalt der -Struktur.

Die Funktion verarbeitet keine Puffer mit dem SECBUFFER \_ READONLY-Attribut.

Die Länge der [**SecBuffer-Struktur,**](/windows/win32/api/sspi/ns-sspi-secbuffer) die die Nachricht enthält, darf nicht größer als **cbMaximumMessage** sein, die von der [**Funktion QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG \_ ATTR STREAM SIZES) abgerufen \_ \_ wird.

Bei Verwendung des Digest-SSP muss ein zweiter Puffer vom Typ SECBUFFER \_ PADDING oder SEC \_ BUFFER DATA \_ vorhanden sein, um [*Signaturinformationen*](../secgloss/d-gly.md#_security_digital_signature_gly) zu speichern. Rufen Sie zum Abrufen der Größe des Ausgabepuffers die [**Funktion QueryContextAttributes (Digest)**](querycontextattributes--digest.md) auf, und geben Sie SECPKG \_ ATTR \_ SIZES an. Die Funktion gibt eine [**SecPkgContext \_ Sizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **Membern cbMaxSignature** und **cbBlockSize.**

Anwendungen, die SSL nicht verwenden, müssen einen [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) vom Typ SECBUFFER \_ PADDING bereitstellen.

</dd> <dt>

*MessageSeqNo* \[ In\]
</dt> <dd>

Die Sequenznummer, die die Transportanwendung der Nachricht zugewiesen hat. Wenn die Transportanwendung keine Sequenznummern verwaltet, muss dieser Parameter 0 (null) sein.

Bei Verwendung des Digest-SSP muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenznummerierung intern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ BUFFER \_ TOO \_ SMALL**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Eine ordnungsgemäß geschriebene Anwendung sollte diesen Fehler nicht erhalten.<br/>                                                                                               |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | Das für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Verschlüsselungsverfahren*](../secgloss/c-gly.md) wird nicht unterstützt.<br/>                                                                                                         |
| <dl> <dt>**SEC \_ E \_ INSUFFICIENT \_ MEMORY**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Ein ungültiges Kontexthandle wurde im *phContext-Parameter* angegeben.<br/>                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ INVALID \_ TOKEN**</dt> </dl>          | Es wurde kein \_ SECBUFFER-DATENTYPpuffer gefunden.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP NICHT \_ \_ UNTERSTÜTZT**</dt> </dl>     | Weder Vertraulichkeit noch [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **EncryptMessage (Digest)-Funktion** verschlüsselt eine Nachricht basierend auf der Nachricht und dem [*Sitzungsschlüssel*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext.*](../secgloss/s-gly.md)

Wenn die Transportanwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenzerkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die Funktion diese Informationen mit der verschlüsselten Nachricht. Das Einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transportanwendung übergeben wird.

Wenn Sie den Digest-SSP verwenden, rufen Sie die Größe des Ausgabepuffers ab, indem Sie die [**QueryContextAttributes (Digest)-Funktion**](querycontextattributes--digest.md) aufrufen und SECPKG \_ ATTR \_ SIZES angeben. Die Funktion gibt eine [**SecPkgContext \_ Sizes-Struktur**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **Membern cbMaxSignature** und **cbBlockSize.**

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

 



| Puffertyp                           | Beschreibung                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_SECBUFFER-STREAMHEADER \_<br/>  | Wird intern verwendet. Keine Initialisierung erforderlich.<br/>                                                                        |
| SECBUFFER \_ DATA<br/>            | Enthält die zu verschlüsselnde [*Klartextnachricht.*](../secgloss/s-gly.md)<br/> |
| SECBUFFER \_ STREAM \_ TRAILER<br/> | Wird intern verwendet. Keine Initialisierung erforderlich.<br/>                                                                        |
| SECBUFFER \_ EMPTY<br/>           | Wird intern verwendet. Keine Initialisierung erforderlich. Die Größe kann 0 (null) sein.<br/>                                                      |



 

Um eine optimale Leistung zu erzielen, sollten die *pMessage-Strukturen* aus zusammenhängendem Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als **SealMessage** bezeichnet. Anwendungen sollten jetzt nur **EncryptMessage (Digest)** verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (Digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (Digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
