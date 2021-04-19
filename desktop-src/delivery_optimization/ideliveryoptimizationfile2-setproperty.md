---
title: 'IDeliveryOptimizationFile2:: SetProperty-Methode'
description: 'Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück. | IDeliveryOptimizationFile2:: SetProperty-Methode'
keywords:
- SetProperty-Methode
- SetProperty-Methode, IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2 Interface, SetProperty-Methode
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
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361815"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2:: SetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*PROPID* \[ in\]
</dt> <dd>

Die erforderliche Eigenschaften-ID, die vom Typ "dofilepropertyid" festgelegt wird.

</dd> <dt>

*propvalue* \[ in\]
</dt> <dd>

Der festzulegende Eigenschafts Wert des Typs Variant.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Erfolg                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte eigen schafts-ID                                                |
| **DO_E_INVALID_STATE**       | Der Auftrag befindet sich derzeit nicht in einem Zustand, der eine Eigenschafts Einstellung zulässt. |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
