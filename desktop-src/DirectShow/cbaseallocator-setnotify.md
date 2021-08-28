---
description: Die SetNotify-Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn. Die Zuweisung ruft die Rückrufmethode auf, wenn die IMemAllocator::ReleaseBuffer-Methode der Zuweisung aufgerufen wird.
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: CBaseAllocator.SetNotify-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16e836be1610e8c2399a263120d847f3fada4b638332ee81914031f7a8e3ffb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108650"
---
# <a name="cbaseallocatorsetnotify-method"></a>CBaseAllocator.SetNotify-Methode

\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Die `SetNotify` -Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn. Die Zuweisung ruft die Rückrufmethode auf, wenn die [**IMemAllocator::ReleaseBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) der Zuweisung aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNotify* 
</dt> <dd>

Zeiger auf die [**IMemAllocatorNotifyCallbackTemp-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) die für den Rückruf verwendet wird. Der Aufrufer muss die -Schnittstelle implementieren. Verwenden Sie den Wert **NULL,** um den Rückruf zu entfernen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die [**IMemAllocatorCallbackTemp::SetNotify-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) Die Zuweisung macht die [**IMemAllocatorCallbackTemp-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) nur verfügbar, wenn das *fEnableReleaseCallback-Flag* im [**CBaseAllocator-Konstruktor**](cbaseallocator.md) auf **TRUE** festgelegt ist.

Diese Methode legt die [**CBaseAllocator::m \_ pNotify-Membervariable**](cbaseallocator-m-pnotify.md) auf *pNotify* fest und erhöht die Verweisanzahl auf der Schnittstelle. Wenn *m \_ pNotify* nicht **NULL** ist, ruft die **ReleaseBuffer-Methode** der Zuweisung [**IMemAllocatorNotifyCallbackTemp::NotifyRelease auf.**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease) Informationen zum Implementieren des Rückrufs finden Sie im Abschnitt "Hinweise" in dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




