---
description: CBaseStreamControl.CBaseStreamControl-Konstruktor – Konstruktormethode.
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
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095848"
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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




