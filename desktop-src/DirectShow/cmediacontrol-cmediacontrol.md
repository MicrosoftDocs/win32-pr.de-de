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
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099208"
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

## <a name="remarks"></a>Bemerkungen

Ordnen Sie den *pName-Parameter* im statischen Speicher zu. Dieser Name wird beim Erstellen und Löschen des Objekts im Debugterminal angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




