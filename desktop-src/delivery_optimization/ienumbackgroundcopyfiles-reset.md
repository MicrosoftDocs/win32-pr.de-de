---
title: IEnumBackgroundCopyFiles Reset-Methode (Deliveryoptimization.h)
description: 'IEnumBackgroundCopyFiles::Reset-Methode: Setzt die Enumerationssequenz auf den Anfang zurück.'
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset-Methode
- Reset-Methode, IEnumBackgroundCopyFiles-Schnittstelle
- IEnumBackgroundCopyFiles-Schnittstelle, Reset-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bcd0fc46d1106feb553c77727f979da1e3002dc2530f1bb37d8c345220c264b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542007"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a>IEnumBackgroundCopyFiles::Reset-Methode

Setzt die Enumerationsfolge auf den Anfang zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM **HRESULT-Werte** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





