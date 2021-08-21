---
title: IBackgroundCopyCallback JobModification-Methode (Deliveryoptimization.h)
description: Übermittlungsoptimierung (DO) ruft Ihre Implementierung der JobModification-Methode auf, wenn der Auftrag geändert wurde.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- JobModification-Methode
- JobModification-Methode, IBackgroundCopyCallback-Schnittstelle
- IBackgroundCopyCallback-Schnittstelle, JobModification-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b5e6e07cdcd561201c1c1c7cf9b5c07a8796eff344746c0a9199527bba5aad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810470"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>IBackgroundCopyCallback::JobModification-Methode

Übermittlungsoptimierung (DO) ruft Ihre Implementierung der [**JobModification-Methode**](https://www.bing.com/search?q=**JobModification**) auf, wenn der Auftrag geändert wurde. Der Dienst generiert dieses Ereignis, wenn Bytes übertragen, Dem Auftrag Dateien hinzugefügt, Eigenschaften geändert oder der Status des Auftrags geändert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pJob* \[ In\]
</dt> <dd>

Enthält die Methoden für den Zugriff auf Eigenschaften-, Status- und Statusinformationen des Auftrags. Geben Sie *pJob* nicht frei. DO gibt die Schnittstelle frei, wenn die [**JobModification-Methode**](https://www.bing.com/search?q=**JobModification**) zurückgegeben wird.

</dd> <dt>

*dwReserved* \[ In\]
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode sollte S_OK zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback ist als 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





