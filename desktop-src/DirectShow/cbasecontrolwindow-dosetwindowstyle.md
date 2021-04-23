---
description: Die DoSetWindowStyle-Methode ändert die typischen oder erweiterten Fensterstile.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: CBaseControlWindow.DoSetWindowStyle-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909808"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>CBaseControlWindow.DoSetWindowStyle-Methode

Die `DoSetWindowStyle` -Methode ändert die typischen oder erweiterten Fensterstile.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stil* 
</dt> <dd>

Geeignete Fensterstile.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Wert, der angibt, welche Stile festgelegt werden sollen. Dies muss eine der folgenden Ressourcen sein:



| Bezeichnung | Wert |
|--------------|--------------------------------------|
| \_GWL-STIL   | Rufen Sie die Fensterstile ab.          |
| GWL \_ EXSTYLE | Rufen Sie die erweiterten Fensterstile ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Memberfunktion ruft die Win32 **SetWindowLong-Funktion** auf, um den Fensterstil festzulegen, und zeigt das Fenster dann erneut an der aktuellen Position an. Diese Memberfunktion wird von den [**Memberfunktionen CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) und [**CBaseControlWindow::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




