---
description: Die iscarddatabase-Schnittstelle stellt die Methoden zum Ausführen der Daten Bank Vorgänge des Smartcard-Ressourcen-Managers bereit.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Iscarddatabase-Schnittstelle (scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372827"
---
# <a name="iscarddatabase-interface"></a>Iscarddatabase-Schnittstelle

\[Die **iscarddatabase** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **iscarddatabase** -Schnittstelle stellt die Methoden zum Ausführen der Daten Bank Vorgänge des [*Smartcard*](../secgloss/s-gly.md) [*-Ressourcen-Managers*](../secgloss/r-gly.md) bereit. Zu diesen Vorgängen gehören das Auflisten bekannter Smartcards, [*Leser*](../secgloss/r-gly.md)und Lesergruppen sowie das Abrufen der Schnittstellen, die von einer Smartcard und Ihrem [*primären Dienstanbieter*](../secgloss/p-gly.md)unterstützt werden.

> [!Note]  
> Der Bezeichner des primären Dienstanbieters ist eine com-GUID, die zum Instanziieren und Verwenden der COM-Objekte für eine bestimmte Karte verwendet werden kann.

 

Das folgende Beispiel zeigt eine typische Verwendung der **iscarddatabase** -Schnittstelle. In diesem Fall wird die **iscarddatabase** -Schnittstelle verwendet, um alle bekannten Smartcards aufzulisten.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **iscarddatabase** -Schnittstelle.
2.  Rufen Sie [**listcards**](iscarddatabase-listcards.md) auf, um alle bekannten Smartcards auf der Grundlage einer [*ATR-Zeichenfolge*](../secgloss/a-gly.md) oder ihrer unterstützten Schnittstellen abzurufen.
3.  Geben Sie die **iscarddatabase** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscarddatabase** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscarddatabase** verfügt auch über die folgenden Typen von Mitgliedern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscarddatabase** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getprovidercardid**](iscarddatabase-getprovidercardid.md)   | Ruft den Bezeichner des [*primären Dienstanbieters*](../secgloss/p-gly.md) für eine bestimmte Smartcard ab.<br/> |
| [**Listcardinterfaces**](iscarddatabase-listcardinterfaces.md) | Ruft die Schnittstellen Bezeichner (GUIDs) aller Schnittstellen ab, die von einer bestimmten Smartcard unterstützt werden.<br/>                                                                                 |
| [**Listcards**](iscarddatabase-listcards.md)                   | Ruft alle smartcardnamen ab, die einem bestimmten Satz von Schnittstellen Bezeichnerzeichen (GUIDs) oder einer [*ATR-Zeichenfolge*](../secgloss/a-gly.md)entsprechen.<br/> |
| [**Listreadergroups**](iscarddatabase-listreadergroups.md)     | Ruft die Namen der [*Lesergruppen*](../secgloss/r-gly.md) ab, die dem Ressourcen-Manager bekannt sind.<br/>                        |
| [**Listreaders**](iscarddatabase-listreaders.md)               | Rufen Sie die Namen der [*Leser*](../secgloss/r-gly.md) ab, von denen der Ressourcen-Manager wissen hat.<br/>                                          |



 

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
| IID<br/>                      | IID \_ iscarddatabase ist als 1461aac8-6810-11D0-918f -00aa00c18068 definiert.<br/>       |



 

 
