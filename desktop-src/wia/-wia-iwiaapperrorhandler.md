---
description: Mit der IWiaAppErrorHandler-Schnittstelle können Anwendungen Fehlerfenster (während Datenübertragungen) anzeigen, in denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: IWiaAppErrorHandler-Schnittstelle (Wia.h)
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
ms.openlocfilehash: 385a97a71d7017cba5bbfffd0833068a74acbe9d7281f8308b003a525b3f60f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441346"
---
# <a name="iwiaapperrorhandler-interface"></a>IWiaAppErrorHandler-Schnittstelle

Mit der **IWiaAppErrorHandler-Schnittstelle** können Anwendungen Fehlerfenster (während Datenübertragungen) anzeigen, in denen der Benutzer auswählen kann, ob die Übertragung fortgesetzt, abgebrochen oder abgebrochen werden soll.

## <a name="members"></a>Member

Die **IWiaAppErrorHandler-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaAppErrorHandler** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaAppErrorHandler-Schnittstelle** verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und mindestens eine Schaltfläche zum Fortsetzen, Abbrechen oder Abbrechen der Anwendung bereitstellt.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Behandelt Gerätestatus- und Fehlermeldungen während Bilddatenübertragungen und zeigt die Meldungen dem Benutzer an.<br/>                                  |



 

## <a name="remarks"></a>Hinweise

Das Fehlerbehandlungs- oder Rückrufobjekt, das diese Schnittstelle implementiert, wird an [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) und [**IWiaTransfer::Hochladen**](-wia-iwiatransfer-upload.md)übergeben.

Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb von Bilddatenübertragungen auftreten, z. B. Fehler beim Abrufen oder Festlegen von Geräteeigenschaften oder nicht ausgeführte Rückrufe in einem Treiber.

Ein Treiberfehlerhandler sollte [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)anstelle von **IWiaAppErrorHandler** implementieren.

Das Objekt, das diese Schnittstelle implementiert, sollte auch [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)implementieren.

Wenn Sie möchten, dass ein Treiberfehlerhandler und ein Standardfehlerhandler Fehlermeldungsfenster anzeigen, aber keinen vollständigen Fehlerhandler für die Anwendung erstellen möchten, implementieren Sie diese Schnittstelle und implementieren auch die [**IWiaAppErrorHandler::ReportStatus-Methode,**](-wia-iwiaapperrorhandler-reportstatus.md) um WIA \_ STATUS NOT HANDLED \_ \_ zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
