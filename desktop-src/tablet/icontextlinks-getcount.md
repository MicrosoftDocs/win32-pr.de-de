---
description: Ruft die Anzahl der IContextLink-Objekte in dieser Auflistung ab.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: IContextLinks::GetCount-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c622e3b222aacb2b05b56a4fbe933d0578ee6649b3a5f5d84a3c5d9b6382c629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092281"
---
# <a name="icontextlinksgetcount-method"></a>IContextLinks::GetCount-Methode

Ruft die Anzahl der [**IContextLink-Objekte**](icontextlink.md) in dieser Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ out, retval\]
</dt> <dd>

Die Anzahl der [**IContextLink-Objekte,**](icontextlink.md) die in dieser Auflistung enthalten sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




