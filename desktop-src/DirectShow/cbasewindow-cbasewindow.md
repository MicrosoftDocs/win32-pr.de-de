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
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095818"
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

## <a name="remarks"></a>Bemerkungen

Nachdem Sie das -Objekt erstellt haben, rufen Sie die [**CBaseWindow::P repareWindow-Methode**](cbasewindow-preparewindow.md) auf, um das Fenster zu erstellen. **PrepareWindow** ist eine virtuelle Methode. Sie ruft [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md)auf, ebenfalls eine virtuelle Methode. Diese Methoden werden vom Konstruktor getrennt, sodass abgeleitete Klassen sie bei Bedarf überschreiben können.

Wenn der Wert des *bDoGetDC-Parameters* **TRUE** ist, ruft das `CBaseWindow` -Objekt ein Handle für den Gerätekontext (DC) des Fensters ab und speichert es in der [**CBaseWindow::m \_ hdc-Membervariablen.**](cbasewindow-m-hdc.md) Das -Objekt erstellt auch einen kompatiblen Speicherdomänencontroller, der in der [**Membervariablen CBaseWindow::m \_ MemoryDC**](cbasewindow-m-memorydc.md) gespeichert wird. Diese Aktionen treten in der **InitialiseWindow-Methode** auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




