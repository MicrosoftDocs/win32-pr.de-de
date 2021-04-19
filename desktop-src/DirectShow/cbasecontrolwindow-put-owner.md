---
description: Die Put \_ Owner-Methode legt das übergeordnete Fenster des Videofensters fest. das übergeordnete Fenster leitet dann bestimmte Meldungen an das Videofenster weiter.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359752"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Cbasecontrolwindow. Put \_ Owner-Methode

Die `put_Owner` -Methode legt das übergeordnete Fenster des Videofensters fest. das übergeordnete Fenster leitet dann bestimmte Meldungen an das Videofenster weiter.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Besitzer* 
</dt> <dd>

Handle für das übergeordnete Fenster.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt noError zurück.

## <a name="remarks"></a>Bemerkungen

Intern ruft diese Methode die Microsoft Win32 **SetParent** -Funktion auf, um den neuen Besitzer festzulegen, und legt den Stil des übergeordneten Fensters auf WS \_ Child fest. Das übergeordnete Fenster führt dann bestimmte Nachrichten Sätze (insbesondere Maus-und Tastatur Meldungen) an das Videofenster weiter.

Nachdem Sie den Besitzer des Videofensters festgelegt haben, müssen Sie für den Besitzer den Wert **null** festlegen, und der Fenster Stil des Besitzers muss auf WS überlappende \_ und WS clipchildren festgelegt werden, \_ bevor das Filter Diagramm freigegeben wird. Wenn Sie den Besitzer auf **null** festlegen, deaktiviert diese Methode das untergeordnete WS-Bit des übergeordneten Fensters \_ . Wenn Sie den Besitzer nicht auf **null** festlegen, übergibt das übergeordnete Fenster weiterhin Meldungen an das Videofenster, und es treten wahrscheinlich Fehler auf, wenn die Anwendung geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




