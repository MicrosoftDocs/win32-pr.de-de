---
description: Die InitialiseWindow-Methode initialisiert das Fenster.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.InitialiseWindow-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954659"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.InitialiseWindow-Methode

Die `InitialiseWindow` -Methode initialisiert das Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle zum Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Standardmäßig ruft diese Methode ein Handle für den Gerätekontext (DC) des Fensters ab und erstellt einen kompatiblen Speicherdomänencontroller. Wenn der Wert des [**Flags CBaseWindow::m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md) **FALSE** ist, ruft diese Methode die Gerätekontexte jedoch nicht ab. Der Arbeitsspeicher-DC ist nützlich, um Bitmaps auszuwählen, bevor sie in das Fenster geblittert werden.

Die [**CBaseWindow::D oCreateWindow-Methode**](cbasewindow-docreatewindow.md) ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




