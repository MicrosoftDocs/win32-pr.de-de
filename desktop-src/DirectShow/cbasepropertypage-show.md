---
description: 'Die Show-Methode zeigt das Dialogfeld an oder blendet es aus. Diese Methode implementiert die IPropertyPage:: Show-Methode.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Cbasepropertypage. Show-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365690"
---
# <a name="cbasepropertypageshow-method"></a>Cbasepropertypage. Show-Methode

Die- `Show` Methode zeigt das Dialogfeld an oder blendet es aus. Diese Methode implementiert die [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) -Methode.

## <a name="syntax"></a>Syntax

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Parameter

*nCmdShow*

Typ: **[uint](../winprog/windows-data-types.md)**

Ein Wert, der angibt, ob das Fenster angezeigt oder ausgeblendet werden soll. Weitere Informationen finden Sie unter der [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) -Methode.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.

| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument.<br/>   |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/> |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Cbasepropertypage-Klasse](cbasepropertypage.md)
