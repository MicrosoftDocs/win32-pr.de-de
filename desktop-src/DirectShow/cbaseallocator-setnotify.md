---
description: 'Die setnotify-Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn. Die Zuweisung Ruft die Rückruf Methode auf, wenn die imemzuzuordcator:: ReleaseBuffer-Methode der Zuweisung aufgerufen wird.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Cbasezucator. setnotify-Methode (amfilter. h)
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
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360986"
---
# <a name="cbaseallocatorsetnotify-method"></a>Cbasezucator. setnotify-Methode

\[[**Setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Die- `SetNotify` Methode legt einen Rückruf für die Zuweisung fest oder entfernt ihn. Die Zuweisung Ruft die Rückruf Methode auf, wenn die [**imemzuzuordcator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode der Zuweisung aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnotify* 
</dt> <dd>

Ein Zeiger auf die Schnittstelle [**imemzucallbacktemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) , die für den Rückruf verwendet wird. Der Aufrufer muss die-Schnittstelle implementieren. Verwenden Sie den Wert **null** , um den Rückruf zu entfernen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die [**imemzuzucallorcallbacktemp:: setnotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) -Methode. [**Die Zuweisung**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) wird von der Zuweisung nicht verfügbar gemacht, es sei denn, das *fenablereleasecallback* -Flag ist im [**cbasezucator**](cbaseallocator.md) -Konstruktor auf **true** festgelegt.

Diese Methode legt die [**cbasezucator:: m \_ pnotify**](cbaseallocator-m-pnotify.md) -Member-Variable auf *pnotify* fest und erhöht den Verweis Zähler für die Schnittstelle. Wenn *m \_ pnotify* nicht **null** ist, ruft die **ReleaseBuffer** -Methode des zuordcators [**imemzucatornotifycallbacktemp:: notifyrelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease)auf. Weitere Informationen zum Implementieren des Rückrufs finden Sie im Abschnitt "Hinweise" in dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




