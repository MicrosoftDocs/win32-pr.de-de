---
title: IBackgroundCopyManager-Schnittstelle (Deliveryoptimization.h)
description: Erstellt Übertragungsaufträge, ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- IBackgroundCopyManager-Schnittstelle
- IBackgroundCopyManager-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cf1ca14443823a5448a63c04d19d00957d4064353183d79aa7762f729115301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542152"
---
# <a name="ibackgroundcopymanager-interface"></a>IBackgroundCopyManager-Schnittstelle

Erstellt Übertragungsaufträge, ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.

## <a name="members"></a>Member

Die **IBackgroundCopyManager-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyManager** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyManager-Schnittstelle** verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Erstellt einen Übertragungsauftrag.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Ruft einen angegebenen Auftrag aus der Warteschlange ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager ist als 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

