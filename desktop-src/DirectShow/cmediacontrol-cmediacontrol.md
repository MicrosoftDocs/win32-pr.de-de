---
description: 'CMediaControl.CMediaControl-Konstruktor : Konstruktormethode.'
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: CMediaControl.CMediaControl-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afc31e6d2803632cf2b92d3346fe9d73f3ddb3b5cfab3436fedeee56ab79797a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635045"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>CMediaControl.CMediaControl-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen des Objekts zu Debugzwecken.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ordnen Sie den *pName-Parameter* im statischen Speicher zu. Dieser Name wird beim Erstellen und Löschen des Objekts im Debugterminal angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




