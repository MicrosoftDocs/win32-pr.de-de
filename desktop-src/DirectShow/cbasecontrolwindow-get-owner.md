---
description: Mit der Methode "Get Owner" wird \_ der aktuelle Fenster Besitzer abgerufen.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370710"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Cbasecontrolwindow. get \_ Owner-Methode

Die- `get_Owner` Methode ruft den aktuellen Fenster Besitzer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Besitzer* 
</dt> <dd>

Zeiger auf den Fenster Besitzer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Videofenster kann innerhalb einer Dokument Umgebung wiedergegeben werden. Zu diesem Zweck muss das Fenster als untergeordnetes Element eines anderen Fensters erstellt werden (sodass es abgeschnitten und entsprechend verschoben wird). Mit dieser Eigenschaft kann der Besitzer des Fensters festgelegt und abgerufen werden. Wenn das Fenster im Besitz eines anderen Fensters ist, wird einfach die Microsoft Win32-Funktion " **SetParent** " aufgerufen. Eine Anwendung, die diese Funktion aufrufen, ändert die Fenster Stile, um das untergeordnete WS-Bit festzulegen \_ .

Wenn sich das Fenster im Besitz eines anderen Fensters befindet, werden automatisch bestimmte Nachrichten Sätze (insbesondere Maus-und Tastatur Meldungen) weiterleiten. Dies ermöglicht es einer Anwendung, eine einfache Bearbeitung von Hot-Spot und andere Interaktionen durchzuführen.

Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden. Rufen Sie die Member-Funktion [**cbasecontrolwindow:: getownerwindow**](cbasecontrolwindow-getownerwindow.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




