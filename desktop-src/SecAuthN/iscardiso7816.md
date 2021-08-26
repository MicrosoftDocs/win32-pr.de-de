---
description: Die ISCardISO7816-Schnittstelle stellt Methoden zum Implementieren von ISO 7816-4-Funktionen bereit.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: ISCardISO7816-Schnittstelle (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aeda73e926ca9276e7e41ecfe966a088e311f4077040abe9eadb4ffc1701bfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014340"
---
# <a name="iscardiso7816-interface"></a>ISCardISO7816-Schnittstelle

\[Die **ISCardISO7816-Schnittstelle** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardISO7816-Schnittstelle** stellt Methoden zum Implementieren von ISO 7816-4-Funktionen bereit. Mit Ausnahme von [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)erstellen diese Methoden einen APDU-Befehl [*(Application Protocol Data Unit),*](../secgloss/a-gly.md) der in einem [**ISCardCmd-Objekt**](iscardcmd.md) gekapselt ist.

Die ISO 7816-4-Spezifikation definiert Standardbefehle, die auf [*Smartcards*](../secgloss/s-gly.md)verfügbar sind. Die Spezifikation definiert auch, wie ein Smartcard-APDU-Befehl erstellt und zur Ausführung an die Smartcard gesendet werden soll. Diese Schnittstelle automatisiert den Erstellungsprozess.

Das folgende Beispiel zeigt eine typische Verwendung der **ISCardISO7816-Schnittstelle.** In diesem Fall wird die **ISCardISO7816-Schnittstelle** verwendet, um einen APDU-Befehl zu erstellen.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **ISCardISO7816-** und [**ISCardCmd-Schnittstelle.**](iscardcmd.md)

    Die [**ISCardCmd-Schnittstelle**](iscardcmd.md) wird verwendet, um die APDU zu kapseln.

2.  Rufen Sie die entsprechende Methode der **ISCardISO7816-Schnittstelle** auf, und übergeben Sie dabei die erforderlichen Parameter und den [**ISCardCmd-Schnittstellenzeiger.**](iscardcmd.md)

    Der ISO 7816-4-APDU-Befehl wird erstellt und in der [**ISCardCmd-Schnittstelle**](iscardcmd.md) gekapselt.

3.  Geben Sie die Schnittstellen **ISCardISO7816** und [**ISCardCmd**](iscardcmd.md) frei.

> [!Note]  
> Wenn auf den Methodenverweisseiten keine Bitsequenz in einer Tabelle definiert ist, gehen Sie davon aus, dass die Bitsequenz für die zukünftige Verwendung oder proprietär für einen bestimmten Anbieter reserviert ist.

 

## <a name="members"></a>Member

Die **ISCardISO7816-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardISO7816** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardISO7816-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Erstellt einen Befehl, der einen Datensatz am Ende einer elementaren Datei (EF) anfügt.<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Legt einen Teil des Inhalts eines EF sequenziell auf seinen logischen gelöschten Zustand fest, beginnend mit einem angegebenen Offset.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Aktualisiert den Sicherheitsstatus bedingt mithilfe des Ergebnisses der Berechnung durch die Karte, basierend auf einer Zuvor von der Karte ausgegebenen Abfrage (z. B. durch den INS \_ GET \_ CHALLENGE-Befehl), einem möglicherweise geheimen Schlüssel, der auf der Karte gespeichert ist, und Authentifizierungsdaten, die vom Schnittstellengerät übertragen werden.<br/> |
| [**GetChallenge**](iscardiso7816-getchallenge.md)                 | Erfordert das Ausstellen einer Abfrage für die Verwendung in einem sicherheitsrelevanten Verfahren.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Ruft basierend auf dem angegebenen Dateityp ein einzelnes primitives Datenobjekt oder einen Satz von Datenobjekten ab, die in einem konstruierten Datenobjekt enthalten sind.<br/>                                                                                                                                                          |
| [**Getresponse**](iscardiso7816-getresponse.md)                   | Überträgt von der Karte an die Schnittstellengeräte-APDUs, die andernfalls nicht von den verfügbaren Protokollen übertragen werden konnten.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Initiiert die Berechnung der Authentifizierungsdaten durch die Karte unter Verwendung der vom Schnittstellengerät gesendeten Abfragedaten und eines relevanten geheimnisses, das auf der Karte gespeichert ist.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Öffnet und schließt logische Kanäle.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Speichert ein primitives Datenobjekt oder mindestens ein Datenobjekt, das in einem konstruierten Datenobjekt enthalten ist, innerhalb des aktuellen [*Ressourcen-Manager-Kontexts.*](../secgloss/r-gly.md)<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Erstellt einen Befehl, der eine Antwortnachricht erhält, die diesen Teil des Inhalts eines EF mit transparenter Struktur angibt.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Erstellt einen Befehl, der den Inhalt der angegebenen Datensätze einer elementaren Datei liest.<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | Legt eine aktuelle Datei innerhalb eines logischen Kanals fest.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Weist ein Standardklassen-ID-Byte zu, das in allen Vorgängen beim Erstellen einer ISO 7816-4-Befehls-APDU verwendet wird.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Initiiert die Aktualisierung der Bits, die bereits in einem EF vorhanden sind, mit den Bits, die im Befehls-APDU angegeben sind.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Erstellt einen Befehl, der die Aktualisierung eines bestimmten Datensatzes initiiert.<br/>                                                                                                                                                                                                                                  |
| [**Überprüfung**](iscardiso7816-verify.md)                             | Initiiert den Vergleich der vom Schnittstellengerät gesendeten Überprüfungsdaten auf der Karte mit den auf der Karte gespeicherten Verweisdaten.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Initiiert das Schreiben von binären Werten in eine EF.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Erstellt einen Befehl, der einen Datensatz schreibt.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53B6AA68-3F56-11D0-916B-00AA00C18068 definiert.<br/>        |



 

 
