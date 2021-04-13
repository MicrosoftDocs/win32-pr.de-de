---
description: Ermöglicht das Öffnen und Verwalten einer Verbindung mit einer Smartcard.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Iscard-Schnittstelle (scardmgr. h)
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
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528151"
---
# <a name="iscard-interface"></a>Iscard-Schnittstelle

\[Die **iscard** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der **iscard** -Schnittstelle können Sie eine Verbindung zu einer [*Smartcard*](../secgloss/s-gly.md)öffnen und verwalten. Für jede Verbindung mit einer Karte ist eine einzelne, entsprechende Instanz der **iscard** -Schnittstelle erforderlich.

Der Smartcard- [*Ressourcen-Manager*](../secgloss/r-gly.md) muss immer verfügbar sein, wenn eine Instanz von **iscard** erstellt wird. Wenn dieser Dienst nicht verfügbar ist, tritt bei der Erstellung der-Schnittstelle ein Fehler auf.

Das folgende Beispiel zeigt eine typische Verwendung der **iscard** -Schnittstelle. Die **iscard** -Schnittstelle wird verwendet, um eine Verbindung mit der Smartcard herzustellen, eine [*Transaktion*](../secgloss/t-gly.md)zu senden und die Smartcard freizugeben.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **iscard** -Schnittstelle.
2.  Fügen Sie an eine Smartcard an, indem Sie einen [*Smartcardleser*](../secgloss/r-gly.md) oder ein zuvor ermitteltes, gültiges Handle angeben.
3.  Erstellen Sie Transaktions Befehle mit [**iscardcmd**](iscardcmd.md)-und [**ISCardISO7816**](iscardiso7816.md) -smartcardschnittstellen.
4.  Verwenden Sie **iscard** , um die Transaktions Befehle zur Verarbeitung durch die Smartcard zu übermitteln.
5.  Verwenden Sie **iscard** , um die Smartcard freizugeben.
6.  Geben Sie die **iscard** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscard** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. Die **iscard** verfügt auch über die folgenden Arten von Mitgliedern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iscard** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachbyhandle**](iscard-attachbyhandle.md) | Fügt ein-Objekt an ein geöffnetes und konfiguriertes smartcardhandle an.<br/>                                                                                                                                                      |
| [**Attachbyreader**](iscard-attachbyreader.md) | Öffnet die Smartcard im benannten Reader.<br/>                                                                                                                                                                            |
| [**Trennen**](iscard-detach.md)                 | Schließt die geöffnete Verbindung mit der Smartcard.<br/>                                                                                                                                                                        |
| [**Sperrkarte**](iscard-lockscard.md)           | Anspruchs exklusiver Zugriff auf die Smartcard.<br/>                                                                                                                                                                           |
| [**Erneut**](iscard-reattach.md)             | Setzt die Smartcard zurück und initialisiert sie erneut.<br/>                                                                                                                                                                             |
| [**Transaktion**](iscard-transaction.md)       | Führt einen Schreib-und Lesevorgang für den smartcardbefehl ([*Application Protocol Data Unit*](../secgloss/a-gly.md)) aus.<br/> |
| [**Unlockcard**](iscard-unlockscard.md)       | Gibt exklusiven Zugriff auf die Smartcard frei.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Die **iscard** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Schreibgeschützt<br/> | Ruft die [*ATR-Zeichenfolge*](../secgloss/a-gly.md) der Smartcard ab.<br/>                                                                   |
| [**Cardhandle**](iscard-get-cardhandle.md)<br/> | Schreibgeschützt<br/> | Ruft das Handle für die verbundene Smartcard ab.<br/>                                                                                                                                  |
| [**Kontext**](iscard-get-context.md)<br/>       | Schreibgeschützt<br/> | Ruft das aktuelle [*Resource Manager-Kontext*](../secgloss/r-gly.md) Handle ab.<br/>                            |
| [**Protokoll**](iscard-get-protocol.md)<br/>     | Schreibgeschützt<br/> | Ruft den Bezeichner des zurzeit auf der Smartcard verwendeten Protokolls ab.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Schreibgeschützt<br/> | Ruft den aktuellen [*Zustand*](../secgloss/s-gly.md) der [*Smartcard*](../secgloss/s-gly.md) ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068<br/>               |



 

 
