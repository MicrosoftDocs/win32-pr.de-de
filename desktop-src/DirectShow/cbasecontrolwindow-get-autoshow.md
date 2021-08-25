---
description: Die get \_ AutoShow-Methode ruft das aktuelle AutoShow-Statusflag ab.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: CBaseControlWindow.get_AutoShow-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a5c16e0b460d07255cae113194f672ca3dace6f46827ac613c9559370284beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158793"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow.get \_ AutoShow-Methode

Die `get_AutoShow` -Methode ruft das aktuelle AutoShow-Statusflag ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Autoshow* 
</dt> <dd>

Zeiger auf ein boolesches Automation-Flag (0 ist deaktiviert, 1 ist aktiviert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IVideoWindow::get \_ AutoShow-Methode.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) Diese Eigenschaft vereinfacht den Fensteranzeigezugriff für Anwendungen. Wenn dies auf 1 (ein) festgelegt ist, wird das Fenster, das normalerweise nach der Verbindung des Filters ausgeblendet wird, automatisch angezeigt, wenn der Filter angehalten oder ausgeführt wird. Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter beendet wird. Wenn dieser Parameter auf 0 (deaktiviert) festgelegt ist, wird das Fenster nur sichtbar gemacht, wenn die Anwendung [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.

Diese Memberfunktion soll von externen Objekten über die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) aufgerufen werden und sperrt daher den kritischen Abschnitt für die Synchronisierung mit dem zugeordneten Filter. Rufen Sie die [**CBaseControlWindow::IsAutoShowEnabled-Memberfunktion**](cbasecontrolwindow-isautoshowenabled.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht aus einem externen Objekt aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




