---
title: IDeliveryOptimizationFile2::SetProperty-Methode
description: Diese Methode gibt eine einzelne Eigenschaft der DO-Datei zurück. | IDeliveryOptimizationFile2::SetProperty-Methode
keywords:
- SetProperty-Methode
- SetProperty-Methode, IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2-Schnittstelle, SetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635720"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2::SetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft der DO-Datei zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*propId* \[ In\]
</dt> <dd>

Die erforderliche Eigenschaften-ID, die vom Typ DOFilePropertyId festgelegt werden soll.

</dd> <dt>

*propValue* \[ In\]
</dt> <dd>

Der festzulegende Eigenschaftswert vom Typ VARIANT.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Erfolg                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte Eigenschaften-ID                                                |
| **DO_E_INVALID_STATE**       | Der Auftrag befindet sich derzeit nicht in einem Zustand, der eine Eigenschafteneinstellung zulässt. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10, nur Desktop-Apps der Version 1803 \[\]                                   |
| Unterstützte Mindestversion (Server)  | Windows Server, nur Desktop-Apps der Version 1709 \[\]                               |
| Header                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Bibliothek                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 ist als 18995A26-BF59-4ABE-9F8B-D5092D5A2405 definiert. |

## <a name="see-also"></a>Siehe auch

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
