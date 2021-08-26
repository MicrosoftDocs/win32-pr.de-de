---
description: Ermöglicht ihnen das Öffnen und Verwalten einer Verbindung mit einer Smartcard.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: ISCard-Schnittstelle (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68015cc4e834aaa1baaec0046a472d5a290cb22b0d0879e6d6f2fccfd9d21d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015540"
---
# <a name="iscard-interface"></a>ISCard-Schnittstelle

\[Die **ISCard-Schnittstelle** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Mit der **ISCard-Schnittstelle** können Sie eine Verbindung mit einer [*Smartcard*](../secgloss/s-gly.md)öffnen und verwalten. Jede Verbindung mit einer Karte erfordert eine einzelne, entsprechende Instanz der **ISCard-Schnittstelle.**

Der [*Smartcardressourcen-Manager*](../secgloss/r-gly.md) muss immer verfügbar sein, wenn eine Instanz von **ISCard** erstellt wird. Wenn dieser Dienst nicht verfügbar ist, schlägt die Erstellung der Schnittstelle fehl.

Das folgende Beispiel zeigt eine typische Verwendung der **ISCard-Schnittstelle.** Die **ISCard-Schnittstelle** wird verwendet, um eine Verbindung mit der Smartcard herzustellen, eine [*Transaktion*](../secgloss/t-gly.md)zu übermitteln und die Smartcard freizugeben.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **ISCard-Schnittstelle.**
2.  Fügen Sie an eine Smartcard an, indem Sie einen [*Smartcardleser*](../secgloss/r-gly.md) angeben oder ein zuvor eingerichtetes, gültiges Handle verwenden.
3.  Erstellen Sie Transaktionsbefehle mit den Smartcardschnittstellen [**ISCardCmd**](iscardcmd.md)und [**ISCardISO7816.**](iscardiso7816.md)
4.  Verwenden Sie **ISCard,** um die Transaktionsbefehle zur Verarbeitung durch die Smartcard zu übermitteln.
5.  Verwenden Sie **ISCard,** um die Smartcard freizugeben.
6.  Geben Sie die **ISCard-Schnittstelle** frei.

## <a name="members"></a>Member

Die **ISCard-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCard** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ISCard-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Fügt ein Objekt an ein geöffnetes und konfiguriertes Smartcardhandle an.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Öffnet die Smartcard im benannten Reader.<br/>                                                                                                                                                                            |
| [**Trennen**](iscard-detach.md)                 | Schließt die geöffnete Verbindung mit der Smartcard.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Beansprucht exklusiven Zugriff auf die Smartcard.<br/>                                                                                                                                                                           |
| [**Anfügen**](iscard-reattach.md)             | Setzt die Smartcard zurück und initialisiert sie erneut.<br/>                                                                                                                                                                             |
| [**Transaktion**](iscard-transaction.md)       | Führt einen Schreib- und Lesevorgang für das Smartcard-Befehlsobjekt [*(Anwendungsprotokoll-Dateneinheit)*](../secgloss/a-gly.md)aus.<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Gibt exklusiven Zugriff auf die Smartcard frei.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Die **ISCard-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Schreibgeschützt<br/> | Ruft die [*ATR-Zeichenfolge*](../secgloss/a-gly.md) der Smartcard ab.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Schreibgeschützt<br/> | Ruft das Handle für die verbundene Smartcard ab.<br/>                                                                                                                                  |
| [**Kontext**](iscard-get-context.md)<br/>       | Schreibgeschützt<br/> | Ruft das aktuelle [*Resource Manager-Kontexthandle*](../secgloss/r-gly.md) ab.<br/>                            |
| [**Protokoll**](iscard-get-protocol.md)<br/>     | Schreibgeschützt<br/> | Ruft den Bezeichner des Protokolls ab, das derzeit auf der Smartcard verwendet wird.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Schreibgeschützt<br/> | Ruft den aktuellen [*Zustand*](../secgloss/s-gly.md) ab, in dem sich die [*Smartcard*](../secgloss/s-gly.md) befindet.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



 

 
