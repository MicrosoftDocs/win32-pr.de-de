---
title: Ideliveryoptimizationjob-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ideliveryoptimizationjob-Schnittstelle, um Bereiche einer Datei herunterzuladen.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Ideliveryoptimizationjob-Schnittstelle
- Ideliveryoptimizationjob-Schnittstelle, beschrieben
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
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103653"
---
# <a name="ideliveryoptimizationjob-interface"></a>Ideliveryoptimizationjob-Schnittstelle

Verwenden Sie die **ideliveryoptimizationjob** -Schnittstelle, um Bereiche einer Datei herunterzuladen.

## <a name="members"></a>Member

Die **ideliveryoptimizationjob** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ideliveryoptimizationjob** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ideliveryoptimizationjob** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**ADDFILEWITHRANGES**](ideliveryoptimizationjob-addfilewithranges.md) | Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert.<br/>         |



 

