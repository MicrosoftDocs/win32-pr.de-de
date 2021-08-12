---
description: Die Get \_ Owner-Methode ruft den aktuellen Fensterbesitzer ab.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner -Methode (Ctlutil.h)
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
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660513"
---
# <a name="cbasecontrolwindowget_owner-method"></a>CBaseControlWindow.get \_ Owner-Methode

Die `get_Owner` -Methode ruft den aktuellen Fensterbesitzer ab.

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

Zeiger auf den Fensterbesitzer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Das Videofenster kann innerhalb einer Dokumentumgebung wieder verwendet werden. Dazu muss das Fenster zu einem untergeordneten Fenster eines anderen Fensters werden (damit es abgeschnitten und entsprechend verschoben wird). Mit dieser Eigenschaft kann der Besitzer des Fensters festgelegt und abgerufen werden. Wenn sich das Fenster im Besitz eines anderen Fensters befindet, ruft es einfach die Microsoft Win32 **SetParent-Funktion** auf. Eine Anwendung, die diese Funktion aufruft, ändert die Fensterstile, um das WS \_ CHILD-Bit auf zu setzen.

Wenn sich das Fenster im Besitz eines anderen Fensters befindet, werden bestimmte Nachrichtensätze (insbesondere Maus- und Tastaturnachrichten) automatisch weitergeleitet. Dadurch kann eine Anwendung einfache Hot-Spot-Bearbeitungen und andere Interaktionen ermöglichen.

Diese Memberfunktion soll von externen Objekten über die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) aufgerufen werden und sperrt daher den kritischen Abschnitt für die Synchronisierung mit dem zugeordneten Filter. Rufen Sie [**die CBaseControlWindow::GetOwnerWindow-Memberfunktion**](cbasecontrolwindow-getownerwindow.md) auf, um diese Eigenschaft abzurufen, wenn sie nicht von einem externen Objekt aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




