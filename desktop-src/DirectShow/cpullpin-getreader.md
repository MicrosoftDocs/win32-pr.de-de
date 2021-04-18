---
description: Die GetReader-Methode gibt einen Zeiger auf die iasynkreader-Schnittstelle der Ausgabe-PIN zurück.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Cpullpin. GetReader-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365574"
---
# <a name="cpullpingetreader-method"></a>Cpullpin. GetReader-Methode

Die `GetReader` -Methode gibt einen Zeiger auf die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle der Ausgabe-PIN zurück.

## <a name="syntax"></a>Syntax


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle zurück.

## <a name="remarks"></a>Bemerkungen

Die zurückgegebene Schnittstelle weist einen ausstehenden Verweis Zähler auf. Der Aufrufer muss die-Schnittstelle freigeben.

Die-Methode überprüft nicht den Wert des Schnittstellen Zeigers vor dem Aufrufen von " **adressf**". Rufen Sie diese Methode erst auf, wenn Sie die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode erfolgreich aufgerufen haben. Andernfalls ist der Schnittstellen Zeiger möglicherweise **null** , und der Aufruf von **adressf** löst eine Ausnahme aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




