---
description: Mithilfe der iwiaapperrorhandler-Schnittstelle können Anwendungen Fehler Fenster (während der Datenübertragungen) anzeigen, von denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Iwiaapperrorhandler-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373056"
---
# <a name="iwiaapperrorhandler-interface"></a>Iwiaapperrorhandler-Schnittstelle

Mithilfe der **iwiaapperrorhandler** -Schnittstelle können Anwendungen Fehler Fenster (während der Datenübertragungen) anzeigen, von denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.

## <a name="members"></a>Member

Die **iwiaapperrorhandler** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiaapperrorhandler** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiaapperrorhandler** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.<br/> |
| [**Report Status**](-wia-iwiaapperrorhandler-reportstatus.md) | Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.<br/>                                  |



 

## <a name="remarks"></a>Bemerkungen

Die Fehlerbehandlung oder das Rückruf Objekt, das diese Schnittstelle implementiert, wird an [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md) und [**iwiatransfer:: Upload**](-wia-iwiatransfer-upload.md)übergeben.

Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb der Bild Datenübertragungen aufgetreten sind, z. b. Fehler beim Aufrufen oder Festlegen von Geräteeigenschaften oder nicht zurückgegebene Rückrufe an einen Treiber.

Ein Treiber Fehlerhandler sollte [**iwiaerrorhandler**](-wia-iwiaerrorhandler.md)anstelle von **iwiaapperrorhandler** implementieren.

Das Objekt, das diese Schnittstelle implementiert, sollte auch [**iwiatransfercallback**](-wia-iwiatransfercallback.md)implementieren.

Wenn Sie möchten, dass ein Treiber Fehlerhandler und der Standardfehler Handler Fehler Meldungs Fenster anzeigen, aber keinen kompletten Fehlerhandler für die Anwendung erstellen möchten, implementieren Sie diese Schnittstelle, und implementieren Sie außerdem die [**iwiaapperrorhandler:: Report Status**](-wia-iwiaapperrorhandler-reportstatus.md) -Methode, um einen \_ \_ nicht behandelten WIA-Status zurückzugeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
