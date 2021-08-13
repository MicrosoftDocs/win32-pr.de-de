---
title: IDeliveryOptimizationFile2-Schnittstelle
description: IDeliveryOptimizationFile2 unterstützt das Festlegen und Abrufen optionaler Dateieigenschaften.
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
ms.openlocfilehash: ed7409635444885b662688ce94c300aae6e62186dd76bd7278b3e7445ef50c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542045"
---
# <a name="ideliveryoptimizationfile2-interface"></a>IDeliveryOptimizationFile2-Schnittstelle

**IDeliveryOptimizationFile2 unterstützt das Festlegen** und Abrufen optionaler Dateieigenschaften. 

## <a name="members"></a>Member

Die **IDeliveryOptimizationFile2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile2** verfügt auch über diese Membertypen:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDeliveryOptimizationFile2-Schnittstelle** verfügt über diese Methoden.

| Methode                                                 | Beschreibung                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Diese Methode gibt eine einzelne Eigenschaft der DO-Datei zurück. |
| [**Setproperty**](ideliveryoptimizationfile2-setproperty.md)  | Diese Methode legt eine einzelne Eigenschaft der DO-Datei fest.    |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)      | Windows 10 Desktop-Apps, Version 1803 \[\]                                    |
| Unterstützte Mindestversion (Server)      | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                                |
| Header                        | Deliveryoptimization.h                                                            |
| Idl                           | DeliveryOptimization.idl                                                          |
| Bibliothek                       | Dosvc.lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 ist als 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 definiert. |
