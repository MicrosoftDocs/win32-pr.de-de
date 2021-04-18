---
description: Die getaccesstimage-Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Cbasecontrolvideo. getaccesstimage-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365434"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Cbasecontrolvideo. gethapptimage-Methode

Die- `GetCurrentImage` Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbuffersize* 
</dt> <dd>

Ein Zeiger auf die Größe des Ausgabepuffers.

</dd> <dt>

*pvideoimage* 
</dt> <dd>

Zeiger auf den Ausgabepuffer für das Bild.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.



| Rückgabecode                                                                                        | Beschreibung                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>             | Fehler.<br/>                                                               |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>       | Ungültiges Argument.<br/>                                                      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>      | Nicht genügend Arbeitsspeicher. Wird zurückgegeben, wenn der *pvideoinfo* -Parameter **null** ist.<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Erfolg.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl> | Der Vorgang konnte nicht ausgeführt werden, da der Filter nicht angehalten wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion Ruft das Bild aus dem Beispiel ab und kopiert es in den Ausgabepuffer. Der Abschnitt des Videos, das in den Ausgabepuffer kopiert wurde, reflektiert das Quell Rechteck, das über die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Schnittstelle festgelegt Das Ziel Rechteck wird nicht wiederzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




