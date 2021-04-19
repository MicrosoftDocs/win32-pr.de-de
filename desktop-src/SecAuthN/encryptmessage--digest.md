---
description: Verschlüsselt eine Nachricht, um den Datenschutz mithilfe von Digest bereitzustellen.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Verschlüsseltmessage (Digest)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342818"
---
# <a name="encryptmessage-digest-function"></a>Verschlüsseltmessage (Digest)-Funktion

Die Funktion " **verschlüsseltmessage" (Digest)** verschlüsselt eine Nachricht, um [*Datenschutz*](../secgloss/p-gly.md)bereitzustellen. Mit **verschlüsseltmessage (Digest)** kann die Anwendung zwischen [*Kryptografiealgorithmen*](../secgloss/c-gly.md) auswählen, die vom ausgewählten Mechanismus unterstützt werden. Die Funktion " **verschlüsseltmessage (Digest)** " verwendet den [*Sicherheitskontext*](../secgloss/s-gly.md) , auf den vom Kontext Handle verwiesen wird. Einige Pakete enthalten keine Nachrichten, die verschlüsselt oder entschlüsselt werden müssen, sondern stellen einen Integritäts [*Hash*](../secgloss/h-gly.md) bereit, der überprüft werden kann.

Diese Funktion ist nur als SASL-Mechanismus verfügbar.

> [!Note]  
> **Verschlüsseltmessage (Digest)** und [**DecryptMessage (Digest)**](decryptmessage--digest.md) können gleichzeitig von zwei verschiedenen Threads in einem SSPI-Kontext (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) aufgerufen werden, wenn ein Thread verschlüsselt und der andere entschlüsselt wird. Wenn mehrere Threads verschlüsselt werden oder mehr als ein Thread entschlüsselt wird, sollte jeder Thread einen eindeutigen Kontext erhalten.

 

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

*phcontext* \[ in\]
</dt> <dd>

Ein Handle für den [*Sicherheitskontext*](../secgloss/s-gly.md) , der zum Verschlüsseln der Nachricht verwendet werden soll.

</dd> <dt>

vollständig verfügbar  \[ in\]
</dt> <dd>

Paket spezifische Flags, die die Qualität des Schutzes angeben. Ein [*Sicherheitspaket*](../secgloss/s-gly.md) kann diesen Parameter verwenden, um die Auswahl von [*Kryptografiealgorithmen*](../secgloss/c-gly.md)zu aktivieren.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Bei der Eingabe verweist die Struktur auf eine oder mehrere [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Strukturen, die den Typ secbuffer-Daten aufweisen können \_ . Dieser Puffer enthält die zu verschlüsselnde Nachricht. Die Nachricht wird direkt verschlüsselt und überschreibt den ursprünglichen Inhalt der Struktur.

Die Funktion verarbeitet keine Puffer mit dem schreibgeschützten secbuffer- \_ Attribut.

Die Länge der [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Nachricht enthält, darf nicht größer als **cbmaximummess** sein, das von der [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (secpkg \_ attr \_ Stream \_ sizes)-Funktion abgerufen wird.

Bei der Verwendung des Digest-SSP muss ein zweiter Puffer vom Typ "secbuffer \_ Padding" oder "sec"-Puffer Daten vorhanden sein, \_ um die \_ [*Signatur*](../secgloss/d-gly.md#_security_digital_signature_gly) Informationen zu speichern. Um die Größe des Ausgabepuffers abzurufen, nennen Sie die [**QueryContextAttributes-Funktion (Digest)**](querycontextattributes--digest.md) , und geben Sie die Größe der secpkg- \_ attr an \_ . Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.

Anwendungen, die nicht SSL verwenden, müssen einen [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) des Typs secbuffer-Auffüll Zeichen bereitstellen \_ .

</dd> <dt>

*Messageseqno* \[ in\]
</dt> <dd>

Die Sequenznummer, die der Nachricht von der Transport Anwendung zugewiesen wurde. Wenn die Transport Anwendung keine Sequenznummern beibehält, muss dieser Parameter NULL sein.

Wenn Sie den Digest-SSP verwenden, muss dieser Parameter auf 0 (null) festgelegt werden. Der Digest-SSP verwaltet die Sequenz Nummerierung intern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sekunde \_ E \_ Puffer \_ zu \_ klein**</dt> </dl>      | Der Ausgabepuffer ist zu klein. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                 |
| <dl> <dt>**Sek. \_ E \_ Kontext \_ abgelaufen**</dt> </dl>        | Die Anwendung verweist auf einen Kontext, der bereits geschlossen wurde. Diese Fehlermeldung sollte von einer ordnungsgemäß geschriebenen Anwendung nicht empfangen werden.<br/>                                                                                               |
| <dl> <dt>**s \_ E \_ \_ Kryptografiesystem \_ ungültig**</dt> </dl> | Die für den [*Sicherheitskontext*](../secgloss/s-gly.md) ausgewählte [*Chiffre*](../secgloss/c-gly.md) wird nicht unterstützt.<br/>                                                                                                         |
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>    | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>         | Im Parameter " *phcontext* " wurde ein ungültiges Kontext Handle angegeben.<br/>                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>          | Es wurde kein \_ Datentypen Puffer für den secbuffer gefunden.<br/>                                                                                                                                                                                          |
| <dl> <dt>**Sek. \_ E- \_ QoP \_ nicht \_ unterstützt**</dt> </dl>     | Die Vertraulichkeit und [*Integrität*](../secgloss/i-gly.md) werden vom [*Sicherheitskontext*](../secgloss/s-gly.md)nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Funktion **verschlüsseltmessage (Digest)** verschlüsselt eine Nachricht auf der Grundlage der Nachricht und des [*Sitzungsschlüssels*](../secgloss/s-gly.md) aus einem [*Sicherheitskontext*](../secgloss/s-gly.md).

Wenn die Transport Anwendung den [*Sicherheitskontext*](../secgloss/s-gly.md) zur Unterstützung der Sequenz Erkennung erstellt hat und der Aufrufer eine Sequenznummer bereitstellt, enthält die-Funktion diese Informationen mit der verschlüsselten Nachricht. Das einschließen dieser Informationen schützt vor Wiedergabe, Einfügung und Unterdrückung von Nachrichten. Das [*Sicherheitspaket*](../secgloss/s-gly.md) enthält die Sequenznummer, die von der Transport Anwendung zurückgegeben wurde.

Wenn Sie den Digest-SSP verwenden, rufen Sie die Größe des Ausgabepuffers ab, indem Sie die Funktion [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) aufrufen und die Größe der secpkg- \_ attr angeben \_ . Die-Funktion gibt eine [**secpkgcontext \_ sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) -Struktur zurück. Die Größe des Ausgabepuffers ist die Summe der Werte in den **memmaxsignature** -und **cbblocksize** -Membern.

> [!Note]  
> Diese Puffer müssen in der angezeigten Reihenfolge angegeben werden.

 



| Puffertyp                           | BESCHREIBUNG                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| secbuffer \_ - \_ Streamheader<br/>  | Wird intern verwendet. Es ist keine Initialisierung erforderlich.<br/>                                                                        |
| secbuffer- \_ Daten<br/>            | Enthält die zu verschlüsselnde [*Klartext*](../secgloss/s-gly.md) -Nachricht.<br/> |
| secbuffer- \_ streamnachspann \_<br/> | Wird intern verwendet. Es ist keine Initialisierung erforderlich.<br/>                                                                        |
| secbuffer ist \_ leer.<br/>           | Wird intern verwendet. Es ist keine Initialisierung erforderlich. Die Größe kann NULL sein.<br/>                                                      |



 

Um eine optimale Leistung zu erzielen, sollten die *pMessage* -Strukturen aus einem zusammenhängenden Speicher zugeordnet werden.

**Windows XP:** Diese Funktion wurde auch als " **versiesagemessage**" bezeichnet. Anwendungen sollten jetzt nur " **verschlüsseltmessage (Digest)** " verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Akzeptsecuritycontext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (Digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (Digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
