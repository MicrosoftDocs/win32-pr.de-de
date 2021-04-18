---
title: Ideliveryoptimizationfile GetStats-Methode (deliveryoptimization. h)
description: Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats-Methode
- GetStats-Methode, ideliveryoptimizationfile-Schnittstelle
- Ideliveryoptimizationfile-Schnittstelle, GetStats-Methode
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
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392127"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>Ideliveryoptimizationfile:: GetStats-Methode

Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*swarmstats* \[ vorgenommen\]
</dt> <dd>

Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück. Weitere Informationen finden Sie in der Struktur " [**doswarmstats**](doswarmstats.md) ".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte **S_OK** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ideliveryoptimizationfile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





