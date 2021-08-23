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
ms.openlocfilehash: 0fe158e4a17b898110a2555f87b469ee934aa791b6f0379f9054642810673389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793760"
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

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft die Win32 **GetWindowLong-Funktion** auf, um den Fensterstil abzurufen. Sie wird von den [**Memberfunktionen CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) und [**CBaseControlWindow::get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




