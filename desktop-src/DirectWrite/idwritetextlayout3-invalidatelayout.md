---
title: IDWriteTextLayout3 InvalidateLayout-Methode
description: Erklärt das Layout für ungültig und erzwingt, dass das Layout vor dem Aufrufen der Metriken oder Zeichnungsfunktionen neu messen muss. Dies ist nützlich, wenn sich die Lokalität einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn sich die Größe eines von einem Client implementierten IDWriteInlineObject ändert.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- InvalidateLayout-Methode – Direkter Schreibzugriff
- InvalidateLayout-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3-Schnittstelle Direct Write , InvalidateLayout-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816081"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>IDWriteTextLayout3::InvalidateLayout-Methode

Erklärt das Layout für ungültig und erzwingt, dass das Layout vor dem Aufrufen der Metriken oder Zeichnungsfunktionen neu messen muss. Dies ist nützlich, wenn sich die Lokalität einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn sich die Größe eines von einem Client implementierten IDWriteInlineObject ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





