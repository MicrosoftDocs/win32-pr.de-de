---
title: IDeliveryOptimizationJob2::GetProperty-Methode
description: Gibt eine einzelne Eigenschaft des DO-Auftrags zurück.
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
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811251"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2::GetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft des DO-Auftrags zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*propId* \[ In\]
</dt> <dd>

Die erforderliche Eigenschaften-ID, die sie erhalten soll. Nur **DOJobPropertyId_ExtendedErrorInfo** vom Typ VT_BSTR werden unterstützt.

</dd> <dt>

*propValue* \[ out\]
</dt> <dd>

Der resultierende Eigenschaftswert, der in einem VARIANT-Typ gespeichert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung          |
|------------------------------|----------------------|
| **S_OK**                     | Erfolg              |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte Eigenschaften-ID. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]                                   |
| Unterstützte Mindestversion (Server)  | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                               |
| Header                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Bibliothek                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 ist als 18995A26-BF59-4ABE-9F8B-D5092D5A2405 definiert. |

## <a name="see-also"></a>Siehe auch

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
