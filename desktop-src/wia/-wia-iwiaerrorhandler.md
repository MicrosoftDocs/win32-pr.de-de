---
description: Die iwiaerrorhandler-Schnittstelle stellt Methoden bereit, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten anfordert, ob für die Vorschau oder die endgültige Bits.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Iwiaerrorhandler-Schnittstelle (WIA. h)
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
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130012"
---
# <a name="iwiaerrorhandler-interface"></a>Iwiaerrorhandler-Schnittstelle

Die **iwiaerrorhandler** -Schnittstelle stellt Methoden bereit, um Fehler zu behandeln, die auftreten können, wenn eine Anwendung Bilddaten anfordert, ob für die Vorschau oder die endgültige Bits.

## <a name="members"></a>Member

Die **iwiaerrorhandler** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiaerrorhandler** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiaerrorhandler** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatus Description**](-wia-iwiaerrorhandler-getstatusdescription.md) | Gibt eine Zeichenfolge zurück, die den Statuscode beschreibt.<br/>                                             |
| [**Report Status**](-wia-iwiaerrorhandler-reportstatus.md)                 | Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Anwendungs Rückruf Objekt kann **iwiaerrorhandler** implementieren.

Diese Schnittstelle ist nicht für die Behandlung von Fehlern konzipiert, die außerhalb der Bild Datenübertragungen aufgetreten sind, z. b. Fehler beim Aufrufen oder Festlegen von Geräteeigenschaften oder nicht zurückgegebene Rückrufe an einen Treiber.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
