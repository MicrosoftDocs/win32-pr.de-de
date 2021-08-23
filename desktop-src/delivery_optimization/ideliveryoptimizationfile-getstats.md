---
title: IDeliveryOptimizationFile GetStats-Methode (Deliveryoptimization.h)
description: Gibt Download- und Uploadstatistiken für eine bestimmte Datei zurück.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats-Methode
- GetStats-Methode, IDeliveryOptimizationFile-Schnittstelle
- IDeliveryOptimizationFile-Schnittstelle, GetStats-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4e2f0a3b680e682944740cb570bfb4889b22ba8e7ec56d3aefc9e34fcdd6a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635760"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>IDeliveryOptimizationFile::GetStats-Methode

Gibt Download- und Uploadstatistiken für eine bestimmte Datei zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*swarmStats* \[ out\]
</dt> <dd>

Gibt Download- und Uploadstatistiken für eine bestimmte Datei zurück. Weitere Informationen finden Sie in der [**DOSwarmStats-Struktur.**](doswarmstats.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte **S_OK** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





