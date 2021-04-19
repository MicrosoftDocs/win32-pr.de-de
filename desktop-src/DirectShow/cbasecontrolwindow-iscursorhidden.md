---
description: Die iscurrsorhidden-Methode ruft den aktuellen Zustand des m \_ bcurrsorhidden-Datenmembers ab.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Cbasecontrolwindow. iscurrsorhidden-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367146"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>Cbasecontrolwindow. iscurrsorhidden-Methode

Die- `IsCursorHidden` Methode ruft den aktuellen Zustand des **m \_ bcurrsorhidden** -Datenmembers ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor ausgeblendet* 
</dt> <dd>

Zeiger auf den Wert von **m \_ bcurrsorhidden**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Aufruf ohne einen-Parameter erfolgt, wird oatrue zurückgegeben, wenn der Cursor ausgeblendet ist, oder oafalse, wenn der Cursor sichtbar ist.

## <a name="remarks"></a>Bemerkungen

Interne Objekte sollten diese Member-Funktion ohne den " *Cursor Hidden* "-Parameter aufrufen, um zu vermeiden, dass der kritische Abschnitt gesperrt wird. Externe Objekte greifen mithilfe des *Cursor* -Parameters über die [**IVideoWindow:: iscurrsorhidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) -Methode auf diese Member-Funktion zu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




