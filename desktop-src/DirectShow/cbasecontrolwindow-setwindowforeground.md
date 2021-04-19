---
description: Mit der setwindowfore-Methode wird das Videofenster in den Vordergrund verschoben, und der Fokus erhält optional den Fokus.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Cbasecontrolwindow. setwindowvorder-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369281"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>Cbasecontrolwindow. setwindowvorder Grund-Methode

Die `SetWindowForeground` -Methode verschiebt das Videofenster in den Vordergrund und gibt ihm optional den Fokus.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fokus* 
</dt> <dd>

Ein Wert, der angibt, ob das Videofenster den Fokus erhält. Der Wert 1 gibt dem Fenster Fokus und 0 nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>                                          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>          | Der Fokus ist nicht gleich 1 oder 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Der aktuelle Filter ist nicht mit einem kompletten Filter Diagramm verbunden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




