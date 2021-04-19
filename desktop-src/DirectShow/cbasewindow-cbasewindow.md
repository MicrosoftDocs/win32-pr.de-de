---
description: Konstruktormethode.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Cbasewindow. cbasewindow-Konstruktor (winutil. h)
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
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359252"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Cbasewindow. cbasewindow-Konstruktor

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

*bdogetdc* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Gerätekontext abgerufen werden soll.

</dd> <dt>

*bpostto Destroy* 
</dt> <dd>

Boolescher Wert, der die [**cbasewindow:: m \_ bdopostdedestroy**](cbasewindow-m-bdoposttodestroy.md) -Element Variable angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nachdem Sie das-Objekt erstellt haben, rufen Sie die [**cbasewindow::P Analyse Window**](cbasewindow-preparewindow.md) -Methode auf, um das-Fenster zu erstellen. **Preparewindow** ist eine virtuelle Methode. [**Cbasewindow:: initialicwindow**](cbasewindow-initialisewindow.md)wird auch als virtuelle Methode aufgerufen. Diese Methoden werden vom-Konstruktor getrennt, sodass abgeleitete Klassen Sie ggf. überschreiben können.

Wenn der Wert des *bdogetdc* -Parameters " **true**" ist, ruft das- `CBaseWindow` Objekt ein Handle für den Gerätekontext des Fensters ab und speichert es in der [**cbasewindow:: m-Element Variablen ( \_ hdc**](cbasewindow-m-hdc.md) ). Das-Objekt erstellt außerdem einen kompatiblen Arbeitsspeicher-DC, der in der Element Variablen [**cbasewindow:: m \_ memorydc**](cbasewindow-m-memorydc.md) gespeichert wird. Diese Aktionen treten in der **initialierwindow** -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




