---
title: IDeliveryOptimizationJob-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie die IDeliveryOptimizationJob-Schnittstelle, um Bereiche einer Datei herunterzuladen.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- IDeliveryOptimizationJob-Schnittstelle
- IDeliveryOptimizationJob-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71f978be993e21ad487af5469327b5f66804166a7e5247dffb841f7815b2279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895680"
---
# <a name="ideliveryoptimizationjob-interface"></a>IDeliveryOptimizationJob-Schnittstelle

Verwenden Sie die **IDeliveryOptimizationJob-Schnittstelle,** um Bereiche einer Datei herunterzuladen.

## <a name="members"></a>Member

Die **IDeliveryOptimizationJob-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationJob** verfügt auch über diese Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDeliveryOptimizationJob-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Fügt einem Downloadauftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962B3EF7 definiert.<br/>         |



 

