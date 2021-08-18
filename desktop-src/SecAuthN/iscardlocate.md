---
description: Die ISCardLocate-Schnittstelle stellt Dienste zum Suchen einer Smartcard anhand ihres Namens bereit.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: ISCardLocate-Schnittstelle (Scardmgr.h)
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
ms.openlocfilehash: 70679a2decc62011df70e68c119365bb8a98f7bdb06af6d7989eac18e7c14fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922929"
---
# <a name="iscardlocate-interface"></a>ISCardLocate-Schnittstelle

\[Die **ISCardLocate-Schnittstelle** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardLocate-Schnittstelle** stellt Dienste zum Suchen einer [*Smartcard*](../secgloss/s-gly.md) anhand ihres Namens bereit.

Diese Schnittstelle kann die [*Smartcard-Benutzeroberfläche*](../secgloss/u-gly.md) anzeigen, falls erforderlich.

Das folgende Szenario zeigt eine typische Verwendung der **ISCardLocate-Schnittstelle.** Die **ISCardLocate-Schnittstelle** wird verwendet, um eine [*Anwendungsprotokolldateneinheit*](../secgloss/a-gly.md) (Application Protocol Data Unit, APDU) zu erstellen.

**So suchen Sie eine bestimmte Karte mit ihrem Namen**

1.  Erstellen Sie eine **ISCardLocate-Schnittstelle.**
2.  Rufen [**Sie ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) auf, um nach einem Smartcardnamen zu suchen.
3.  Rufen [**Sie FindCard**](iscardlocate-findcard.md) auf, um nach der Smartcard zu suchen.
4.  Interpretieren der Ergebnisse
5.  Geben Sie die **ISCardLocate-Schnittstelle** frei.

## <a name="members"></a>Member

Die **ISCardLocate-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardLocate** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardLocate-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Für die zukünftige Verwendung reserviert.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Gibt den Kartennamen an, der bei der Suche verwendet werden soll.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Sucht nach der Smartcard und öffnet eine gültige Verbindung mit ihr.<br/> |



 

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
| IID<br/>                      | IID \_ ISCardLocate ist als 1461AACD-6810-11D0-918F-00AA00C18068 definiert.<br/>         |



 

 
