---
title: IBackgroundCopyJob GetDisplayName-Methode (Deliveryoptimization.h)
description: Ruft den Anzeigenamen für den Auftrag ab. In der Regel verwenden Sie den Anzeigenamen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName-Methode
- GetDisplayName-Methode, IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, GetDisplayName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755540"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>IBackgroundCopyJob::GetDisplayName-Methode

Ruft den Anzeigenamen für den Auftrag ab. In der Regel verwenden Sie den Anzeigenamen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDisplayName* \[ out\]
</dt> <dd>

Auf NULL endende Zeichenfolge, die den Anzeigenamen enthält, der den Auftrag identifiziert. Mehr als ein Auftrag kann den gleichen Anzeigenamen aufweisen. Rufen Sie die [**CoTaskMemFree-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um *ppDisplayName* frei zu machen, wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** sowie andere zurück.



| Rückgabecode                                                                                  | Beschreibung                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK</dt> </dl>     | Der Anzeigename wurde erfolgreich abgerufen.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Der *ppDisplayName-Parameter* darf nicht **NULL** sein.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

