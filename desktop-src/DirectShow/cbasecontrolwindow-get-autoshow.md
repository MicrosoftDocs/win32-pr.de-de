---
description: Die get \_ AutoShow-Methode ruft das aktuelle Autoshow State-Flag ab.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: CBaseControlWindow.get_AutoShow-Methode (ctlutil. h)
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
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372253"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>Cbasecontrolwindow. get \_ AutoShow-Methode

Die- `get_AutoShow` Methode ruft das aktuelle Autoshow State-Flag ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Automatisch anzeigen* 
</dt> <dd>

Zeiger auf ein boolesches Automatisierungs Flag (0 ist off, 1 ist on).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) -Methode. Diese Eigenschaft vereinfacht den Fenster Anzeige Zugriff für-Anwendungen. Wenn dieser Wert auf 1 (on) festgelegt ist, wird das Fenster, das in der Regel nach der Verbindungs Herstellung ausgeblendet wird, automatisch angezeigt, wenn der Filter anhält oder ausgeführt wird. Das Fenster sollte jedoch nicht ausgeblendet werden, wenn der Filter angehalten wird. Wenn dieser Parameter auf 0 (Off) festgelegt ist, wird das Fenster nur angezeigt, wenn die Anwendung [**cbasecontrolwindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) oder [**cbasecontrolwindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) mit den entsprechenden Parametern aufruft.

Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden. Rufen Sie die Member-Funktion [**cbasecontrolwindow:: isautoshowenabled**](cbasecontrolwindow-isautoshowenabled.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




