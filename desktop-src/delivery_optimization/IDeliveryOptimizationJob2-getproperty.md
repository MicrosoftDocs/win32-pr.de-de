---
title: 'IDeliveryOptimizationJob2:: GetProperty-Methode'
description: Gibt eine einzelne Eigenschaft des Do-Auftrags zurück.
keywords:
- GetProperty-Methode
- GetProperty-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475933"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2:: GetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft des Do-Auftrags zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*PROPID* \[ in\]
</dt> <dd>

Die erforderliche Eigenschafts-ID, die erhalten werden soll. Nur **DOJobPropertyId_ExtendedErrorInfo** vom Typ VT_BSTR wird unterstützt.

</dd> <dt>

*propvalue* \[ vorgenommen\]
</dt> <dd>

Der resultierende Eigenschafts Wert, der in einem Variant-Typ gespeichert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung          |
|------------------------------|----------------------|
| **S_OK**                     | Erfolg              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte eigen schafts-ID. |

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
