---
title: IDWriteTextLayout3 invalidatelayout-Methode
description: Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden. Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Invalidatelayout-Methode direkt schreiben
- Invalidatelayout-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, invalidatelayout-Methode
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
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104403"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>IDWriteTextLayout3:: invalidatelayout-Methode

Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden. Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





