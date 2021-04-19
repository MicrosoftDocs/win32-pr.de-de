---
description: Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Ccritsec:: m_fTrace Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370322"
---
# <a name="ccritsecm_ftrace-member"></a>Ccritsec:: m \_ ftrace-Member

Boolescher Wert, der angibt, ob diese Sperre verfolgt werden soll.

## <a name="syntax"></a>Syntax


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Bemerkungen

Diese Member-Variable wird nur in der Debugversion der Basisklasse definiert. Wenn der Wert **true** ist, wird eine Ablauf Verfolgung des Sperr Zustands in das Debugprotokoll geschrieben. (Die Debugprotokollierung für kritische Abschnitte muss aktiv sein.) Weitere Informationen finden Sie unter [**dbglocktrace**](dbglocktrace.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccritsec-Klasse**](ccritsec.md)
</dt> </dl>

 

 




