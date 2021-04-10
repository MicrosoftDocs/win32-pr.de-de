---
description: Stellt die Methoden bereit, die zum Erstellen und Verwalten einer Smartcard-APDU (Application Protocol Data Unit) erforderlich sind.
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Iscardcmd-Schnittstelle (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041608"
---
# <a name="iscardcmd-interface"></a>Iscardcmd-Schnittstelle

\[Die **iscardcmd** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **iscardcmd** -Schnittstelle stellt die Methoden bereit, die zum Erstellen und Verwalten einer [*Smartcard*](../secgloss/s-gly.md) -APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) erforderlich sind. Diese Schnittstelle kapselt zwei Puffer:

-   Der APDU-Puffer enthält die Befehlssequenz, die an die Karte gesendet wird.
-   Der apdureply-Puffer enthält Daten, die nach der Ausführung des APDU-Befehls von der Karte zurückgegeben werden (diese Daten werden auch als Rückgabe-APDU bezeichnet).

Das folgende Beispiel zeigt eine typische Verwendung der **iscardcmd** -Schnittstelle. Die **iscardcmd** -Schnittstelle wird zum Erstellen eines APDU verwendet.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine [**iscardschnittstelle**](iscard.md) , und stellen Sie eine Verbindung mit einer Smartcard her.
2.  Erstellen Sie eine **iscardcmd** -Schnittstelle.
3.  Erstellen Sie einen Smartcard-APDU-Befehl mithilfe der [**ISCardISO7816**](iscardiso7816.md) -Schnittstelle oder einer der **iscardcmd** -buildmethoden.
4.  Führen Sie den Befehl auf der Smartcard aus, indem Sie die entsprechende [**iscard**](iscard.md) -Schnittstellen Methode aufrufen.
5.  Wertet die zurückgegebene Antwort aus.
6.  Wiederholen Sie die Prozedur nach Bedarf.
7.  Geben Sie die **iscardcmd** -Schnittstelle und andere nach Bedarf frei.

## <a name="members"></a>Member

Die **iscardcmd** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardcmd** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iscardcmd** -Schnittstelle verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Buildcmd**](iscardcmd-buildcmd.md)       | Erstellt einen gültigen APDU-Befehl für die Übertragung an eine Smartcard.<br/>                               |
| [**Klartext**](iscardcmd-clear.md)             | Löscht APDU-und Antwort-APDU-Nachrichten Puffer.<br/>                                             |
| [**Kapseln**](iscardcmd-encapsulate.md) | Kapselt den angegebenen APDU-Befehl für die Übertragung an eine Smartcard in einen anderen Befehl-APDU.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iscardcmd** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Alternativen Klassifizierungs-ID**](iscardcmd-get-alternateclassid.md)<br/> | Lesen/Schreiben<br/> | Aktueller Wert der alternativen Klassen-ID.<br/>                                                                                                                        |
| [**APDU**](iscardcmd-get-apdu.md)<br/>                         | Lesen/Schreiben<br/> | RAW [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU).<br/> |
| [**Apdulength**](iscardcmd-get-apdulength.md)<br/>             | Schreibgeschützt<br/>  | Länge der APDU.<br/>                                                                                                                                      |
| [**Apdureply**](iscardcmd-get-apdureply.md)<br/>               | Lesen/Schreiben<br/> | [*Antwort-APDU*](../secgloss/r-gly.md).<br/>                                                                        |
| [**Apdureplylength**](iscardcmd-get-apdureplylength.md)<br/>   | Lesen/Schreiben<br/> | Länge der Antwort-APDU.<br/>                                                                                                                                |
| [**ClassID**](iscardcmd-get-classid.md)<br/>                   | Lesen/Schreiben<br/> | Die Klassen-ID des APDU.<br/>                                                                                                                                    |
| [**Daten**](iscardcmd-get-data.md)<br/>                         | Schreibgeschützt<br/>  | Datenfeld des APDU.<br/>                                                                                                                                  |
| [**Instructionid**](iscardcmd-get-instructionid.md)<br/>       | Lesen/Schreiben<br/> | Anweisungs-ID-Byte aus dem APDU.<br/>                                                                                                                       |
| [**Lefield**](iscardcmd-get-lefield.md)<br/>                   | Schreibgeschützt<br/>  | Le-Feld der APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lesen/Schreiben<br/> | Knotenadresse.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lesen/Schreiben<br/> | Erstes Parameter Byte der APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lesen/Schreiben<br/> | Zweites Parameter Byte der APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Schreibgeschützt<br/>  | Drittes Parameter Byte der APDU.<br/>                                                                                                                        |
| [**Replynad**](iscardcmd-get-replynad.md)<br/>                 | Lesen/Schreiben<br/> | Die von der Karte in der Antwortnachricht verwendete Knotenadresse.<br/>                                                                                                      |
| [**Replystatus**](iscardcmd-get-replystatus.md)<br/>           | Lesen/Schreiben<br/> | [*Antworten Sie den APDU*](../secgloss/r-gly.md) -Nachrichten Status Word.<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Schreibgeschützt<br/>  | Antwort "Message SW1 Status Byte" von APDU.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Schreibgeschützt<br/>  | Antwort "Message SW2 Status Byte" von APDU.<br/>                                                                                                                    |
| **Type**<br/>                                                   | Schreibgeschützt<br/>  | Für die zukünftige Verwendung reserviert.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



 

 
