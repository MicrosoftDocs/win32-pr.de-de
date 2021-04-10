---
title: IDeliveryOptimizationFile2-Schnittstelle
description: Der IDeliveryOptimizationFile2 unterstützt das Festlegen und das erhalten Optionaler Dateieigenschaften.
keywords:
- IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040377"
---
# <a name="ideliveryoptimizationfile2-interface"></a>IDeliveryOptimizationFile2-Schnittstelle

Der **IDeliveryOptimizationFile2** unterstützt das Festlegen und das erhalten Optionaler Dateieigenschaften. 

## <a name="members"></a>Member

Die **IDeliveryOptimizationFile2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IDeliveryOptimizationFile2** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDeliveryOptimizationFile2** -Schnittstelle verfügt über diese Methoden.

| Methode                                                 | BESCHREIBUNG                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Diese Methode legt eine einzelne Eigenschaft der do-Datei fest.    |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)      | Windows 10, Version 1803, \[ nur Desktop-Apps\]                                    |
| Unterstützte Mindestversion (Server)      | Windows Server, Version 1709, \[ nur Desktop-Apps\]                                |
| Header                        | Deliveryoptimization. h                                                            |
| IDL                           | Deliveryoptimization. idl                                                          |
| Bibliothek                       | Dosvc. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 ist als 3a87296f -6ec2-4126-ab29-E3F 8dc4cc390 definiert. |
