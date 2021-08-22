---
title: IDeliveryOptimizationFile2::GetProperty-Methode
description: Diese Methode gibt eine einzelne Eigenschaft der DO-Datei zurück. | IDeliveryOptimizationFile2::GetProperty-Methode
keywords:
- GetProperty-Methode
- GetProperty-Methode, IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542090"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2::GetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft der DO-Datei zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*propId* \[ In\]
</dt> <dd>

Die erforderliche Eigenschaften-ID, um den Typ DOFilePropertyId zu erhalten.

</dd> <dt>

*propValue* \[ out\]
</dt> <dd>

Der in einer VARIANT-Eigenschaft gespeicherte Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Erfolg                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte Eigenschaften-ID.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | Die Eigenschaft ist "Write only" und kann nicht gelesen werden.      |
| **E_NOT_SET**                | Mit der SetProperty-Methode wurde keine Eigenschaft festgelegt. |
| **E_OUTOFMEMORY**            |  Fehler bei der Speicherbelegung                          |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|---------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)  | Windows 10 Desktop-Apps, Version 1803 \[\]                                   |
| Unterstützte Mindestversion (Server)  | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                               |
| Header                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Bibliothek                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 ist als 18995A26-BF59-4ABE-9F8B-D5092D5A2405 definiert. |

## <a name="see-also"></a>Weitere Informationen

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
