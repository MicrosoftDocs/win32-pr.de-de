---
description: Flag, das angibt, ob das Fenster seine Zerstörungs Nachricht postet oder sendet.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Cbasewindow:: m_bDoPostToDestroy Member (winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359676"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Cbasewindow:: m \_ bdopostdedestroy-Member

Flag, das angibt, ob das Fenster seine Zerstörungs Nachricht postet oder sendet. **True** gibt an, dass die [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) -Methode die **PostMessage** -Funktion verwendet, um sich selbst eine private Zerstörungs Nachricht zu senden. **False** gibt an, dass **donewithwindow** die **SendMessage** -Funktion verwendet, um die Nachricht zu senden. Standardmäßig ist der Wert **false**.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




