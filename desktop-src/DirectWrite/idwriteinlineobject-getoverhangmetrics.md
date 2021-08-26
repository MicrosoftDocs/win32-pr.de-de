---
title: IDWriteInlineObject GetOverhangMetrics-Methode
description: IDWriteTextLayout ruft diese Rückruffunktion auf, um die sichtbaren Erweiterungen (in DIPs) des Inlineobjekts abzurufen. Bei einer einfachen Bitmap ohne Auffüllung und ohne Überhänge sind alle Überhänge einfach Nullen.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- GetOverhangMetrics-Methode Direct Write
- GetOverhangMetrics-Methode Direct Write , IDWriteInlineObject-Schnittstelle
- IDWriteInlineObject-Schnittstelle Direct Write , GetOverhangMetrics-Methode
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
ms.openlocfilehash: 011794fc3804435dd565a00035247436814c41474c60b66f90c5cb5d9594f6c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928150"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>IDWriteInlineObject::GetOverhangMetrics-Methode

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ruft diese Rückruffunktion auf, um die sichtbaren Erweiterungen (in DIPs) des Inlineobjekts abzurufen. Bei einer einfachen Bitmap ohne Auffüllung und ohne Überhänge sind alle Überhänge einfach Nullen.

Die Überhänge sollten relativ zur gemeldeten Größe des Objekts zurückgegeben werden (siehe [**DWRITE \_ INLINE \_ OBJECT \_ METRICS)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)und nicht baseline angepasst werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Überhänge* \[ out\]
</dt> <dd>

Typ: **[ **DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Überschreitung von sichtbaren Erweiterungen (in DIPs) außerhalb des -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

