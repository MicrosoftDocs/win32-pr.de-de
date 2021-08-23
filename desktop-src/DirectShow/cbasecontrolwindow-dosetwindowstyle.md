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
ms.openlocfilehash: d3b1f72ace792f13f88fbf0ce1e0edaf7b08789ecba88aede0b4094e9e75ae52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640880"
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

Wert, der an gibt, welche Stile festgelegt werden. Dies muss eine der folgenden Ressourcen sein:



| Bezeichnung | Wert |
|--------------|--------------------------------------|
| \_GWL-STIL   | Rufen Sie die Fensterstile ab.          |
| GWL \_ EXSTYLE | Rufen Sie die erweiterten Fensterstile ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft die **Win32-Funktion SetWindowLong** auf, um den Fensterstil zu festlegen, und zeigt das Fenster dann an der aktuellen Position erneut an. Diese Memberfunktion wird von den [**Memberfunktionen CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) und [**CBaseControlWindow::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




