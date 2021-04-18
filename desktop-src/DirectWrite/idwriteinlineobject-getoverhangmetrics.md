---
title: Idwrite teinlineobject gedeverhangmetrics-Methode
description: Idwrite tetextlayout ruft diese Rückruffunktion auf, um die sichtbaren Blöcke (in Dips) des Inline Objekts abzurufen. Im Fall einer einfachen Bitmap ohne Auffüll-und nicht Überlastung werden alle Überhängen einfach als Nullen angezeigt.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Getverhangmetrics-Methode direkt schreiben
- Getverhangmetrics-Methode Direct Write, idwrite teinlineobject-Schnittstelle
- Idwrite teinlineobject Interface Direct Write, gedeverhangmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371416"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Idwrite teinlineobject:: gedeverhangmetrics-Methode

[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ruft diese Rückruffunktion auf, um die sichtbaren Blöcke (in Dips) des Inline Objekts abzurufen. Im Fall einer einfachen Bitmap ohne Auffüll-und nicht Überlastung werden alle Überhängen einfach als Nullen angezeigt.

Die über schreibungen sollten relativ zur gemeldeten Größe des Objekts zurückgegeben werden (siehe [**dwrite- \_ Inline \_ \_ objektmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) und sollten nicht an die Baseline angepasst werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*überlastet* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **dwrite- \_ \_ overhängenmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Überschreibung der sichtbaren Blöcke (in Dips) außerhalb des Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idwrite teinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**Idwrite teinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

