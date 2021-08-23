---
description: Die Put \_ Owner-Methode legt das übergeordnete Fenster des Videofensters fest. Das übergeordnete Fenster leitet dann bestimmte Nachrichten an das Videofenster weiter.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner-Methode (Ctlutil.h)
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
ms.openlocfilehash: 8f33e0c26506faea93afc11f51aaba13007c443fc011839efafce436fe9f2b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635892"
---
# <a name="cbasecontrolwindowput_owner-method"></a>CBaseControlWindow.put \_ Owner-Methode

Die `put_Owner` -Methode legt das übergeordnete Fenster des Videofensters fest. Das übergeordnete Fenster leitet dann bestimmte Nachrichten an das Videofenster weiter.

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

Gibt NOERROR zurück.

## <a name="remarks"></a>Hinweise

Intern ruft diese Methode die Microsoft Win32 **SetParent-Funktion** auf, um den neuen Besitzer festzulegen, und legt den Stil des übergeordneten Fensters auf WS \_ CHILD fest. Das übergeordnete Fenster leitet dann bestimmte Nachrichtensätze (insbesondere Maus- und Tastaturmeldungen) an das Videofenster weiter.

Nachdem Sie den Besitzer des Videofensters festgelegt haben, müssen Sie den Besitzer auf **NULL** und den Fensterstil des Besitzers auf WS \_ OVERLAPPED und WS CLIPCHILDREN festlegen, bevor Sie \_ das Filterdiagramm freigeben. Wenn Sie den Besitzer auf **NULL** festlegen, deaktiviert diese Methode das WS CHILD-Bit des übergeordneten \_ Fensters. Wenn Sie den Besitzer nicht auf **NULL** festlegen, übergibt das übergeordnete Fenster weiterhin Nachrichten an das Videofenster, und es treten wahrscheinlich Fehler auf, wenn die Anwendung geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




