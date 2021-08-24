---
description: Die SetWindowForeground-Methode verschiebt das Videofenster in den Vordergrund und gibt ihm optional den Fokus.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: CBaseControlWindow.SetWindowForeground-Methode (Ctlutil.h)
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
ms.openlocfilehash: 87a6768c8864de45d50dc630773b756dfad43759adbf4b09ed8070febd37f4d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635470"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>CBaseControlWindow.SetWindowForeground-Methode

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

Wert, der angibt, ob das Videofenster den Fokus erhält. Der Wert 1 gibt den Fensterfokus und 0 nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Der Fokus entspricht nicht 1 oder 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der aktuelle Filter ist nicht mit einem vollständigen Filterdiagramm verbunden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




