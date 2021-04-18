---
description: Die iscardlocate-Schnittstelle stellt Dienste für die Suche nach einer Smartcard anhand ihres Namens bereit.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Iscardlocate-Schnittstelle (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368825"
---
# <a name="iscardlocate-interface"></a>Iscardlocate-Schnittstelle

\[Die **iscardlocate** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **iscardlocate** -Schnittstelle stellt Dienste für die Suche nach einer [*Smartcard*](../secgloss/s-gly.md) anhand ihres Namens bereit.

Diese Schnittstelle kann die Smartcard- [*Benutzeroberfläche*](../secgloss/u-gly.md) anzeigen, wenn Sie erforderlich ist.

Das folgende Szenario zeigt eine typische Verwendung der **iscardlocate** -Schnittstelle. Die **iscardlocate** -Schnittstelle wird verwendet, um eine [*Anwendungsprotokoll-Dateneinheit*](../secgloss/a-gly.md) (APDU) zu erstellen.

**So suchen Sie eine bestimmte Karte mithilfe Ihres Namens**

1.  Erstellen Sie eine **iscardlocate** -Schnittstelle.
2.  Wenn Sie den Namen "konfigurierter Smartcard" verwenden möchten, müssen Sie " [**konfigurierter**](iscardlocate-configurecardnamesearch.md) Name" konfigurieren.
3.  Ruft [**findcard**](iscardlocate-findcard.md) auf, um nach der Smartcard zu suchen.
4.  Interpretieren der Ergebnisse
5.  Geben Sie die **iscardlocate** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscardlocate** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardlocate** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardlocate** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **Konfigurieren von "Konfigurations-guidsearch"**                                             | Für die zukünftige Verwendung reserviert.<br/>                                        |
| [**Konfigurieren von "Konfigurations namesearch"**](iscardlocate-configurecardnamesearch.md) | Gibt den Namen der Karte an, die bei der Suche verwendet werden soll.<br/>               |
| [**Findcard**](iscardlocate-findcard.md)                               | Sucht nach der Smartcard und öffnet eine gültige Verbindung.<br/> |



 

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
| IID<br/>                      | IID \_ iscardlocate ist als 1461aacd-6810-11D0-918f -00aa00c18068 definiert.<br/>         |



 

 
