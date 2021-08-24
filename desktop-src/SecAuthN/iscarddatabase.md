---
description: Die ISCardDatabase-Schnittstelle stellt die Methoden zum Ausführen der Datenbankvorgänge des Smartcard-Ressourcen-Managers bereit.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: ISCardDatabase-Schnittstelle (Scardmgr.h)
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
ms.openlocfilehash: a5bdad1db29630dcf029aab4fbc3812cfc83e0c69dab33c31edb73e21b297b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577170"
---
# <a name="iscarddatabase-interface"></a>ISCardDatabase-Schnittstelle

\[Die **ISCardDatabase-Schnittstelle** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **ISCardDatabase-Schnittstelle** stellt die Methoden zum Ausführen der Datenbankvorgänge des [*Smartcard-Ressourcen-Managers*](../secgloss/r-gly.md) bereit. [](../secgloss/s-gly.md) Zu diesen Vorgängen gehören [](../secgloss/r-gly.md)das Auflisten bekannter Smartcards, Leser und Lesergruppen sowie das Abrufen der Schnittstellen, die von einer Smartcard und ihrem primären [*Dienstanbieter unterstützt werden.*](../secgloss/p-gly.md)

> [!Note]  
> Der Bezeichner des primären Dienstanbieters ist eine COM-GUID, die zum Instanziieren und Verwenden der COM-Objekte für eine bestimmte Karte verwendet werden kann.

 

Das folgende Beispiel zeigt eine typische Verwendung der **ISCardDatabase-Schnittstelle.** In diesem Fall wird die **ISCardDatabase-Schnittstelle** verwendet, um alle bekannten Smartcards auflisten.

**So übermitteln Sie eine Transaktion an eine bestimmte Karte**

1.  Erstellen Sie eine **ISCardDatabase-Schnittstelle.**
2.  Rufen [**Sie ListCards**](iscarddatabase-listcards.md) auf, um alle bekannten Smartcards basierend auf einer [*ATR-Zeichenfolge oder*](../secgloss/a-gly.md) ihren unterstützten Schnittstellen abzurufen.
3.  Geben Sie die **ISCardDatabase-Schnittstelle** frei.

## <a name="members"></a>Member

Die **ISCardDatabase-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardDatabase** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardDatabase-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Ruft den Bezeichner des primären [*Dienstanbieters für*](../secgloss/p-gly.md) eine bestimmte Smartcard ab.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Ruft die Schnittstellenbezeichner (GUIDs) aller Schnittstellen ab, die von einer bestimmten Smartcard unterstützt werden.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Ruft alle Smartcardnamen ab, die mit einem bestimmten Satz von Schnittstellenbezeichnern (GUIDs) oder einer [*ATR-Zeichenfolge übereinstimmen.*](../secgloss/a-gly.md)<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Ruft die Namen der Lesergruppen [*ab,*](../secgloss/r-gly.md) über die der Ressourcen-Manager verfügt.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Rufen Sie die Namen der Leser [*ab,*](../secgloss/r-gly.md) über die der Ressourcen-Manager verfügt.<br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase ist als 1461AAC8-6810-11D0-918F-00AA00C18068 definiert.<br/>       |



 

 
