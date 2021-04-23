---
description: Die DoGetWindowStyle-Methode ruft die aktuellen normalen oder erweiterten Fensterstile ab.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: CBaseControlWindow.DoGetWindowStyle-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909818"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>CBaseControlWindow.DoGetWindowStyle-Methode

Die `DoGetWindowStyle` -Methode ruft die aktuellen normalen oder erweiterten Fensterstile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStyle* 
</dt> <dd>

Zeiger auf eine Variable, die die Formatinformationen empfängt.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Wert, der an gibt, welche Stile abgerufen werden. Dies muss eine der folgenden Ressourcen sein:



| Bezeichnung | Wert |
|--------------|--------------------------------------|
| \_GWL-STIL   | Rufen Sie die Fensterstile ab.          |
| GWL \_ EXSTYLE | Rufen Sie die erweiterten Fensterstile ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Memberfunktion ruft die Win32 **GetWindowLong-Funktion** auf, um den Fensterstil abzurufen. Sie wird von den [**Memberfunktionen CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) und [**CBaseControlWindow::get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




