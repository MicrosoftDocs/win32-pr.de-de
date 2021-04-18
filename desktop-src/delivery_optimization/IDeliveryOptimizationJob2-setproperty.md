---
title: 'IDeliveryOptimizationJob2:: SetProperty-Methode'
description: Diese Methode wird nicht verwendet.
keywords:
- SetProperty-Methode
- SetProperty-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391971"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>IDeliveryOptimizationJob2:: SetProperty-Methode

Diese Methode wird nicht verwendet.

## <a name="syntax"></a>Syntax

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*PROPID* \[ in\]
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*propvalue* \[ in\]
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn PROPID **DOJobPropertyId_ExtendedErrorInfo** ist, wird der zurückgegebene Wert **DO_E_READ_ONLY_PROPERTY**. andernfalls gibt die Funktion **DO_E_UNKNOWN_PROPERTY_ID** zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10, Version 1803, \[ nur Desktop-Apps\]                                   |
| Unterstützte Mindestversion (Server)  | Windows Server, Version 1709, \[ nur Desktop-Apps\]                               |
| Header                    | Deliveryoptimization. h                                                           |
| IDL                       | Deliveryoptimization. idl                                                         |
| Bibliothek                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert. |

## <a name="see-also"></a>Siehe auch

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
