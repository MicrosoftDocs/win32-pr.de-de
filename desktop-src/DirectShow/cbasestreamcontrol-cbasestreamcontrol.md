---
description: 'CBaseStreamControl.CBaseStreamControl-Konstruktor : Konstruktormethode.'
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: CBaseStreamControl.CBaseStreamControl-Konstruktor (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a6f00fbe3e6a1b230935a208e47497a7e64d508e3cca8228df6471172a7bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983390"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>CBaseStreamControl.CBaseStreamControl-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode. In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




