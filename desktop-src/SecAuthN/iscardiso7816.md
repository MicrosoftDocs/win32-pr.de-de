---
description: Die ISCardISO7816-Schnittstelle stellt Methoden zum Implementieren der ISO 7816-4-Funktionalität bereit.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: ISCardISO7816-Schnittstelle (scardssp. h)
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
ms.openlocfilehash: 09e5dc9e84a36148e240e4ba2d31f04216454994
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756444"
---
# <a name="iscardiso7816-interface"></a>ISCardISO7816-Schnittstelle

\[Die **ISCardISO7816** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **ISCardISO7816** -Schnittstelle stellt Methoden zum Implementieren der ISO 7816-4-Funktionalität bereit. Mit Ausnahme von [**setdefaultclassid**](iscardiso7816-setdefaultclassid.md)erstellen diese Methoden einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der in einem [**iscardcmd**](iscardcmd.md) -Objekt gekapselt ist.

Die Spezifikation ISO 7816-4 definiert Standard Befehle, die auf [*Smartcards*](../secgloss/s-gly.md)verfügbar sind. Die Spezifikation definiert auch, wie ein Smartcard-APDU-Befehl erstellt und zur Ausführung an die Smartcard gesendet werden soll. Diese Schnittstelle automatisiert den Erstellungsprozess.

Das folgende Beispiel zeigt eine typische Verwendung der **ISCardISO7816** -Schnittstelle. In diesem Fall wird die **ISCardISO7816** -Schnittstelle verwendet, um einen APDU-Befehl zu erstellen.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **ISCardISO7816** -und [**iscardcmd**](iscardcmd.md) -Schnittstelle.

    Die [**iscardcmd**](iscardcmd.md) -Schnittstelle wird verwendet, um das APDU zu kapseln.

2.  Verwenden Sie die entsprechende-Methode der **ISCardISO7816** -Schnittstelle, und übergeben Sie dabei die erforderlichen Parameter und den [**iscardcmd**](iscardcmd.md) -Schnittstellen Zeiger.

    Der ISO 7816-4-APDU-Befehl wird in der [**iscardcmd**](iscardcmd.md) -Schnittstelle erstellt und gekapselt.

3.  Geben Sie die Schnittstellen **ISCardISO7816** und [**iscardcmd**](iscardcmd.md) frei.

> [!Note]  
> Wenn in den Methoden Verweis Seiten eine Bitsequenz in einer Tabelle nicht definiert ist, nehmen Sie an, dass die Bitsequenz für die zukünftige Verwendung reserviert ist oder für einen bestimmten Anbieter proprietär ist.

 

## <a name="members"></a>Member

Die **ISCardISO7816** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **ISCardISO7816** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardISO7816** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appenddatensatz**](iscardiso7816-appendrecord.md)                 | Erstellt einen Befehl, der einen Datensatz an das Ende einer elementaren Datei (EF) anfügt.<br/>                                                                                                                                                                                                                       |
| [**Erasebinary**](iscardiso7816-erasebinary.md)                   | Legt einen Teil des Inhalts eines EF-Teils sequenziell auf den logischen Lösch Zustand fest, beginnend bei einem bestimmten Offset.<br/>                                                                                                                                                                                              |
| [**Externalauthenticate**](iscardiso7816-externalauthenticate.md) | Aktualisiert den Sicherheitsstatus bedingt anhand des Ergebnisses der Berechnung durch die Karte, basierend auf einer Herausforderung, die zuvor von der Karte ausgegeben wurde (z. b. mit dem Befehl "in \_ get \_ Challenge"), einem möglicherweise geheimen Schlüssel, der auf der Karte gespeichert ist, und von Authentifizierungsdaten, die vom Schnittstellen Gerät übermittelt werden.<br/> |
| [**Getchallenge**](iscardiso7816-getchallenge.md)                 | Erfordert die Ausgabe einer Herausforderung für die Verwendung in einem sicherheitsbezogenen Verfahren.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Ruft ein einzelnes Primitives Datenobjekt oder einen Satz von Datenobjekten ab, die in einem konstruierten Datenobjekt enthalten sind, basierend auf dem angegebenen Dateityp.<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | Überträgt von der Karte an die APDUs der Schnittstellen Geräte, die andernfalls nicht durch die verfügbaren Protokolle übertragen werden konnten.<br/>                                                                                                                                                                               |
| [**Internalauthenticate**](iscardiso7816-internalauthenticate.md) | Initiiert die Berechnung der Authentifizierungsdaten durch die Karte mithilfe der vom Schnittstellen Gerät gesendeten Anforderungs Daten und eines relevanten Geheimnisses, das in der Karte gespeichert ist.<br/>                                                                                                                                      |
| [**Managechannel**](iscardiso7816-managechannel.md)               | Öffnet und schließt logische Kanäle.<br/>                                                                                                                                                                                                                                                                      |
| [**Putdata**](iscardiso7816-putdata.md)                           | Speichert ein Primitives Datenobjekt oder ein oder mehrere Datenobjekte, die in einem konstruierten Datenobjekt enthalten sind, innerhalb des aktuellen [*Resource Manager-Kontexts*](../secgloss/r-gly.md).<br/>                                                    |
| [**"Read Binary"**](iscardiso7816-readbinary.md)                     | Erstellt einen Befehl, der eine Antwortnachricht abruft, die diesem Teil des Inhalts eines EF-Inhalts eine transparente Struktur übergibt.<br/>                                                                                                                                                                         |
| [**Daten Satz**](iscardiso7816-readrecord.md)                     | Erstellt einen Befehl, der den Inhalt der angegebenen Datensätze einer elementaren Datei liest.<br/>                                                                                                                                                                                                            |
| [**Selectfile**](iscardiso7816-selectfile.md)                     | Legt eine aktuelle Datei innerhalb eines logischen Kanals fest.<br/>                                                                                                                                                                                                                                                           |
| [**Setdefaultclassid**](iscardiso7816-setdefaultclassid.md)       | Weist ein Standard-Klassen-ID-Byte zu, das bei der Erstellung eines ISO 7816-4-Befehls APDU in allen Vorgängen verwendet wird.<br/>                                                                                                                                                                                      |
| [**Updatebinary**](iscardiso7816-updatebinary.md)                 | Initiiert die Aktualisierung der Bits, die bereits in einem EF vorhanden sind, mit den Bits, die im APDU-Befehl angegeben sind.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Erstellt einen Befehl, der die Aktualisierung eines bestimmten Datensatzes initiiert.<br/>                                                                                                                                                                                                                                  |
| [**Weisen**](iscardiso7816-verify.md)                             | Initiiert den Vergleich in der Karte der über das Schnittstellen Gerät gesendeten Überprüfungs Daten mit den Verweis Daten, die auf der Karte gespeichert sind.<br/>                                                                                                                                                                |
| [**"Write Binary"**](iscardiso7816-writebinary.md)                   | Initiiert das Schreiben von Binär Werten in EF.<br/>                                                                                                                                                                                                                                                      |
| [**Beschreibecord**](iscardiso7816-writerecord.md)                   | Erstellt einen Befehl, mit dem ein Datensatz geschrieben wird.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert<br/>        |



 

 
