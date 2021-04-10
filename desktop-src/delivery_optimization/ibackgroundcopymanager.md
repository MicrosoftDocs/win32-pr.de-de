---
title: Ibackgroundcopymanager-Schnittstelle (deliveryoptimization. h)
description: Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, beschrieben
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
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956590"
---
# <a name="ibackgroundcopymanager-interface"></a>Ibackgroundcopymanager-Schnittstelle

Erstellt Übertragungs Aufträge, Ruft ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und ruft einzelne Aufträge aus der Warteschlange ab.

## <a name="members"></a>Member

Die **ibackgroundcopymanager** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ibackgroundcopymanager** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibackgroundcopymanager** -Schnittstelle verfügt über diese Methoden.



| Methode                                                | BESCHREIBUNG                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [**CreateJob**](ibackgroundcopymanager-createjob.md) | Erstellt einen Übertragungs Auftrag.<br/>                   |
| [**GetJob**](ibackgroundcopymanager-getjob.md)       | Ruft einen angegebenen Auftrag aus der Warteschlange ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager ist als 5ce34c0d-0dc9-4c1f -897c-daa1b78cee7c definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

