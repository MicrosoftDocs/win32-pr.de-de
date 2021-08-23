---
title: INapSystemHealthValidationRequest2 GetConfigID-Methode (NapSystemHealthValidator.h)
description: Wird von den System Health Validators (SHVs) verwendet, um die Konfigurations-ID in einer Validierungsanforderung abzurufen.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- GetConfigID-Methode NAP
- GetConfigID-Methode NAP, INapSystemHealthValidationRequest2-Schnittstelle
- INapSystemHealthValidationRequest2-Schnittstelle NAP, GetConfigID-Methode
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
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625980"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2::GetConfigID-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthValidationRequest2::GetConfigId-Methode** wird von den System Health Validators (SHVs) verwendet, um die Konfigurations-ID in einer Validierungsanforderung abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configID* \[ out\]
</dt> <dd>

Bei der Rückgabe ein Zeiger auf UINT32, der eine Konfigurations-ID der SHV enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                  | Beschreibung                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Vorgang erfolgreich.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der configID-Parameter war **NULL.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





