---
description: Die GetOwnerWindow-Methode ruft das handle m hwndOwner des besitzenden Fensters \_ ab.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: CBaseControlWindow.GetOwnerWindow-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432510"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>CBaseControlWindow.GetOwnerWindow-Methode

Die `GetOwnerWindow` -Methode ruft das handle des besitzenden Fensters ab, **m \_ hwndOwner.**

## <a name="syntax"></a>Syntax


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Besitzerfenster zurück.

## <a name="remarks"></a>Hinweise

Ruft das besitzende Fenster ab, ohne die Schnittstellenmethode aufzurufen. Verwenden Sie diese Memberfunktion anstelle von [**CBaseControlWindow::get \_ Owner,**](cbasecontrolwindow-get-owner.md)es sei denn, Sie rufen dies extern über die [**IVideoWindow::get \_ Owner-Methode**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




