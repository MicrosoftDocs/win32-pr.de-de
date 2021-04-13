---
title: 'IDeliveryOptimizationFile2:: GetProperty-Methode'
description: 'Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück. | IDeliveryOptimizationFile2:: GetProperty-Methode'
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
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353728"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2:: GetProperty-Methode

Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück.

## <a name="syntax"></a>Syntax

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*PROPID* \[ in\]
</dt> <dd>

Die erforderliche Eigenschaften-ID, die vom Typ "dofilepropertyid" erhalten werden soll.

</dd> <dt>

*propvalue* \[ vorgenommen\]
</dt> <dd>

Der in einer Variante gespeicherte Eigenschafts Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden HRESULT-Werte zurück.

| Rückgabecode                  | Beschreibung                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Erfolg                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | Unbekannte eigen schafts-ID.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | Die Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.      |
| **E_NOT_SET**                | Mit der SetProperty-Methode wurde keine Eigenschaft festgelegt. |
| **E_OUTOFMEMORY**            |  Fehler bei der Speicher Belegung                          |

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
