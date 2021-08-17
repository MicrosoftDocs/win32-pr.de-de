---
description: Wird zum Anfügen an eine bestimmte Smartcard oder einen bestimmten Reader, zum Erstellen anderer optionaler Schnittstellen zum Ausführen bestimmter Smartcardfunktionen, zum Sperren einer bestimmten Smartcard für die exklusive Verwendung und zum Abrufen des Status einer Smartcard oder eines Readers verwendet.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: ISCardManage-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: c027ae9004a8437f3d182fdef3335c8fbbad67abaab5c15e351520f2ae592818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922649"
---
# <a name="iscardmanage-interface"></a>ISCardManage-Schnittstelle

\[Die **ISCardManage-Schnittstelle** ist ab Windows Server 2008, Windows Vista und Windows Server 2003 mit Service Pack 1 (SP1) und höher nicht mehr verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die folgende Schnittstellendefinition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard-Dienstanbieters*](../secgloss/s-gly.md) [*befolgt werden kann.*](../secgloss/c-gly.md)

Die **ISCardManage-Schnittstelle** muss bereitgestellt werden. Es wird zum Anfügen [](../secgloss/s-gly.md) an eine [](../secgloss/r-gly.md)bestimmte Smartcard oder einen Bestimmten Reader, zum Erstellen anderer optionaler Schnittstellen zum Ausführen bestimmter Smartcardfunktionen, zum Sperren einer bestimmten Smartcard für die exklusive Verwendung und zum Abrufen des Status einer Smartcard oder eines Readers verwendet. Als Gruppe können diese Dienste für die Verwaltung eines klar definierten Kontexts verantwortlich sein, in dem eine Anwendung mit einer Smartcard oder einem Leser [*kommunizieren*](../secgloss/s-gly.md) [*kann.*](../secgloss/r-gly.md)

Im Folgenden finden Sie eine typische Verwendung der **ISCardManage-Schnittstelle.**

**So stellen Sie eine Verbindung mit einer Smartcard**

1.  Erstellen Sie die **ISCardManage-Schnittstelle,** die der Karte zugeordnet ist.
2.  Verbinden einer Smartcard durch Anfügen an einen bestimmten Smartcardleser ([**AttachByIFD**](iscardmanage-attachbyifd.md)) oder mithilfe eines zuvor erworbenen Handles ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Erstellen Sie andere Schnittstellen zum Ausführen von Smartcardvorgängen ([**CreateCardAuth,**](iscardmanage-createcardauth.md) [**CreateFileAccess,**](iscardmanage-createfileaccess.md) [**CreateCHVerification**](iscardmanage-createchverification.md)oder [**CreateInterface**](iscardmanage-createinterface.md)).
4.  Lassen Sie die Karte los ([**Trennen**](iscardmanage-detach.md)).
5.  Geben Sie **die ISCardManage-Schnittstelle** und andere nach Bedarf frei.

## <a name="members"></a>Member

Die **ISCardManage-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardManage** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISCardManage-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Ermöglicht einer Anwendung das Erstellen einer Kommunikationsverbindung mit einer Smartcard mithilfe eines Handles, das vom Smartcard-Ressourcen-Manager [*zurückgegeben wird.*](../secgloss/r-gly.md)<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Ermöglicht es einer Anwendung, die Einrichtung eines Kontexts für einen bestimmten Reader an fordern, auf den mit einem Anzeigenamen verwiesen wird.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Ermöglicht die Erstellung einer [**ISCardAuth-Schnittstelle.**](iscardauth.md)<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Ermöglicht die Erstellung einer [**ISCardVerify-Schnittstelle.**](iscardverify.md)<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Ermöglicht die Erstellung einer [**ISCardFileAccess-Schnittstelle.**](iscardfileaccess.md)<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Ermöglicht die Erstellung einer Schnittstelle.<br/>                                                                                                                                                                                                                            |
| [**Trennen**](iscardmanage-detach.md)                             | Gibt die Anlage an eine bestimmte Smartcard oder einen bestimmten Reader frei, die von [**AttachByHandle**](iscardmanage-attachbyhandle.md) bzw. [**AttachByIFD zugeordnet**](iscardmanage-attachbyifd.md) wird.<br/>                                                                |
| [**Verbindung wiederherstellen**](iscardmanage-reconnect.md)                       | Ermöglicht einer Anwendung das erneute Herstellen einer Verbindung mit [](iscardmanage-detach.md) einer Smartcard oder einem Reader, ohne eine Trennung gefolgt von [**AttachByHandle**](iscardmanage-attachbyhandle.md) bzw. [**AttachByIFD**](iscardmanage-attachbyifd.md) aus geben zu müssen.<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Sperrt eine verbundene Smartcard oder einen Reader für die exklusive Verwendung.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Gibt die exklusive Verwendung der verbundenen Smartcard oder des verbundenen Readers frei.<br/>                                                                                                                                                                                                   |
| [**Status**](iscardmanage-status.md)                             | Ermöglicht einer Anwendung, den aktuellen Status der Smartcard oder des Lesers zu erhalten.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
