---
description: Die IWiaErrorHandler-Schnittstelle stellt Methoden zum Behandeln von Fehlern bereit, die auftreten können, wenn eine Anwendung Bilddaten anfordert, unabhängig davon, ob es sich um Vorschau- oder letzte Bits handelt.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: IWiaErrorHandler-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965589"
---
# <a name="iwiaerrorhandler-interface"></a>IWiaErrorHandler-Schnittstelle

Die **IWiaErrorHandler-Schnittstelle** stellt Methoden zum Behandeln von Fehlern bereit, die auftreten können, wenn eine Anwendung Bilddaten anfordert, unabhängig davon, ob es sich um Vorschau- oder letzte Bits handelt.

## <a name="members"></a>Member

Die **IWiaErrorHandler-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaErrorHandler** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaErrorHandler-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | Beschreibung                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Verarbeitet Status- und Fehlermeldungen während Bilddatenübertragungen und zeigt sie dem Benutzer an.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Anwendungsrückrufobjekt kann **IWiaErrorHandler** implementieren.

Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb von Bilddatenübertragungen auftreten, z. B. Fehler beim Abrufen oder Festlegen von Geräteeigenschaften oder nicht ausgeführte Rückrufe in einem Treiber.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
