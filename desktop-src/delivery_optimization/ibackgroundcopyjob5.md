---
title: IBackgroundCopyJob5-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie diese Schnittstelle, um mehrere optionale Verhaltensweisen eines Auftrags abzufragen oder festzulegen.
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
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461970"
---
# <a name="ibackgroundcopyjob5-interface"></a>IBackgroundCopyJob5-Schnittstelle

Verwenden Sie diese Schnittstelle, um mehrere optionale Verhaltensweisen eines Auftrags abzufragen oder festzulegen.

Rufen Sie zum Abrufen dieser Schnittstelle die **IBackgroundCopyJob::QueryInterface-Methode** mit `__uuidof(IBackgroundCopyJob5)` als Schnittstellenbezeichner auf.

## <a name="members"></a>Member

Die **IBackgroundCopyJob5-Schnittstelle** erbt von [**IBackgroundCopyJob.**](ibackgroundcopyjob-.md) **IBackgroundCopyJob5** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyJob5-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Eine generische Methode zum Abrufen von DO-Auftragseigenschaften.<br/> |
| [**Setproperty**](ibackgroundcopyjob5-setproperty.md) | Eine generische Methode zum Festlegen von DO-Auftragseigenschaften.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 ist als E847030C-BBBA-4657-AF6D-484AA42BF1FE definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





