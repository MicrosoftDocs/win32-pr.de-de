---
title: INapSystemHealthValidationRequest2 getconfigid-Methode (napsystemhealthvalidator. h)
description: Wird von den System Integritätsprüfungen (SHVs) verwendet, um die Konfigurations-ID in einer Validierungs Anforderung abzurufen.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Getconfigid-Methode NAP
- Getconfigid-Methode NAP, INapSystemHealthValidationRequest2-Schnittstelle
- INapSystemHealthValidationRequest2 Interface NAP, getconfigid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340009"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2:: getconfigid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidationRequest2:: getconfigid** -Methode wird von den System Integritätsprüfungen (SHVs) verwendet, um die Konfigurations-ID in einer Validierungs Anforderung abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigID* \[ vorgenommen\]
</dt> <dd>

Bei der Rückgabe ein Zeiger auf UInt32, der eine Konfigurations-ID des SHV enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Vorgang erfolgreich.<br/>                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der ConfigID-Parameter war **null**.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





