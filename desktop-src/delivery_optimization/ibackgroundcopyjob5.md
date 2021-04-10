---
title: IBackgroundCopyJob5-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie diese Schnittstelle, um mehrere optionale Verhalten eines Auftrags abzufragen oder festzulegen.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105326"
---
# <a name="ibackgroundcopyjob5-interface"></a>IBackgroundCopyJob5-Schnittstelle

Verwenden Sie diese Schnittstelle, um mehrere optionale Verhalten eines Auftrags abzufragen oder festzulegen.

Um diese Schnittstelle abzurufen, nennen Sie die **ibackgroundcopyjob:: QueryInterface** -Methode mithilfe von `__uuidof(IBackgroundCopyJob5)` als Schnittstellen Bezeichner.

## <a name="members"></a>Member

Die **IBackgroundCopyJob5** -Schnittstelle erbt von [**ibackgroundcopyjob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyJob5** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Eine generische Methode zum erhalten von Aufgaben Auftrags Eigenschaften.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Eine generische Methode zum Festlegen von Auftrags Eigenschaften.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 ist als E847030C-bbba-4657-AF6D-484aa42bf1fe definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





