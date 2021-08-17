---
description: 'CBaseWindow.CBaseWindow-Konstruktor : Konstruktormethode.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: CBaseWindow.CBaseWindow-Konstruktor (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8873ee896d910d1596138a8d116c93ae0190534bac48b6ceb19165074f07b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016748"
---
# <a name="cbasewindowcbasewindow-constructor"></a>CBaseWindow.CBaseWindow-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Gerätekontext abgerufen werden soll.

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

Boolescher Wert, der die [**Membervariable CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nachdem Sie das -Objekt erstellt haben, rufen Sie die [**CBaseWindow::P repareWindow-Methode**](cbasewindow-preparewindow.md) auf, um das Fenster zu erstellen. **PrepareWindow** ist eine virtuelle Methode. Sie ruft [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md)auf, ebenfalls eine virtuelle Methode. Diese Methoden werden vom Konstruktor getrennt, sodass abgeleitete Klassen sie bei Bedarf überschreiben können.

Wenn der Wert des *bDoGetDC-Parameters* **TRUE** ist, ruft das `CBaseWindow` -Objekt ein Handle für den Gerätekontext (DC) des Fensters ab und speichert es in der [**CBaseWindow::m \_ hdc-Membervariablen.**](cbasewindow-m-hdc.md) Das -Objekt erstellt auch einen kompatiblen Speicherdomänencontroller, der in der [**Membervariablen CBaseWindow::m \_ MemoryDC**](cbasewindow-m-memorydc.md) gespeichert wird. Diese Aktionen treten in der **InitialiseWindow-Methode** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




