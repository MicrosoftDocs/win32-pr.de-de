---
description: Stellt die Methoden bereit, die zum Erstellen und Verwalten einer Smartcard-ApDU (Application Protocol Data Unit) erforderlich sind.
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: ISCardCmd-Schnittstelle (Hidddat.h)
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
ms.openlocfilehash: e6bce160cfb326f0c44b2fca1c6676b895d9eeeec434826d7fc595fc178c47d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008139"
---
# <a name="iscardcmd-interface"></a>ISCardCmd-Schnittstelle

\[Die **ISCardCmd-Schnittstelle** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardCmd-Schnittstelle** stellt die Methoden bereit, die zum Erstellen und Verwalten einer [*Smartcard-APDU*](../secgloss/s-gly.md) [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) erforderlich sind. Diese Schnittstelle kapselt zwei Puffer:

-   Der APDU-Puffer enthält die Befehlssequenz, die an die Karte gesendet wird.
-   Der APDUReply-Puffer enthält Daten, die von der Karte nach Ausführung des APDU-Befehls zurückgegeben werden (diese Daten werden auch als Rückgabe-APDU bezeichnet).

Das folgende Beispiel zeigt eine typische Verwendung der **ISCardCmd-Schnittstelle.** Die **ISCardCmd-Schnittstelle** wird verwendet, um eine APDU zu erstellen.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine [**ISCard-Schnittstelle,**](iscard.md) und stellen Sie eine Verbindung mit einer Smartcard her.
2.  Erstellen Sie eine **ISCardCmd-Schnittstelle.**
3.  Erstellen Sie einen Smartcard-APDU-Befehl mithilfe der [**ISCardISO7816-Schnittstelle**](iscardiso7816.md) oder einer der **ISCardCmd-Buildmethoden.**
4.  Führen Sie den Befehl auf der Smartcard aus, indem Sie die entsprechende [**ISCard-Schnittstellenmethode**](iscard.md) aufrufen.
5.  Werten Sie die zurückgegebene Antwort aus.
6.  Wiederholen Sie die Prozedur nach Bedarf.
7.  Geben Sie die **ISCardCmd-Schnittstelle** und andere nach Bedarf frei.

## <a name="members"></a>Member

Die **ISCardCmd-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardCmd** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ISCardCmd-Schnittstelle** verfügt über diese Methoden.



| Methode                                       | Beschreibung                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Erstellt eine gültige Befehls-APDU für die Übertragung an eine Smartcard.<br/>                               |
| [**Klar**](iscardcmd-clear.md)             | Löscht die APDU- und Antwort-APDU-Nachrichtenpuffer.<br/>                                             |
| [**Kapseln**](iscardcmd-encapsulate.md) | Kapselt die angegebene Befehls-APDU in eine andere Befehls-APDU für die Übertragung an eine Smartcard.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ISCardCmd-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | Beschreibung                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lesen/Schreiben<br/> | Aktueller id-Wert der alternativen Klasse.<br/>                                                                                                                        |
| [**Apdu**](iscardcmd-get-apdu.md)<br/>                         | Lesen/Schreiben<br/> | Unformatierte [*ApDU (Application Protocol Data Unit).*](../secgloss/a-gly.md)<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Schreibgeschützt<br/>  | Länge des APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lesen/Schreiben<br/> | [*Antwort-APDU*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lesen/Schreiben<br/> | Länge des Antwort-APDU.<br/>                                                                                                                                |
| [**Classid**](iscardcmd-get-classid.md)<br/>                   | Lesen/Schreiben<br/> | Klassen-ID der APDU.<br/>                                                                                                                                    |
| [**Daten**](iscardcmd-get-data.md)<br/>                         | Schreibgeschützt<br/>  | Datenfeld der APDU.<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | Lesen/Schreiben<br/> | Anweisungs-ID-Byte aus der APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Schreibgeschützt<br/>  | Le-Feld der APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lesen/Schreiben<br/> | Knotenadresse.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lesen/Schreiben<br/> | Erstes Parameter byte der APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lesen/Schreiben<br/> | Zweites Parameter byte der APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Schreibgeschützt<br/>  | Drittes Parameter byte der APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lesen/Schreiben<br/> | Knotenadresse, die von der Karte in der Antwortnachricht verwendet wird.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Lesen/Schreiben<br/> | [*Antwort-APDU-Meldungsstatuswort.*](../secgloss/r-gly.md)<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Schreibgeschützt<br/>  | Antwort-APDU-Nachricht SW1-Status byte.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Schreibgeschützt<br/>  | Antwort-APDU-Nachrichten-SW2-Status byte.<br/>                                                                                                                    |
| **Typ**<br/>                                                   | Schreibgeschützt<br/>  | Für die zukünftige Verwendung reserviert.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ddat.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Ddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



 

 
