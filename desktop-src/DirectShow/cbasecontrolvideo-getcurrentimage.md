---
description: Die GetCurrentImage-Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: CBaseControlVideo.GetCurrentImage-Methode (Ctlutil.h)
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
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087570"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>CBaseControlVideo.GetCurrentImage-Methode

Die `GetCurrentImage` -Methode ruft eine Kopie des aktuellen Bilds beim Renderer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Zeiger auf die Größe des Ausgabepuffers.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Zeiger auf den Ausgabepuffer für das Bild.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte oder ein anderer nicht aufgeführter Wert sein.



| Rückgabecode                                                                                        | Beschreibung                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>             | Fehler.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Ungültiges Argument.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Nicht genügend Arbeitsspeicher. Wird zurückgegeben, wenn *der pVideoInfo-Parameter* **NULL ist.**<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Erfolg.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ NICHT \_ ANGEHALTEN**</dt> </dl> | Der Vorgang konnte nicht ausgeführt werden, da der Filter nicht angehalten wurde.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft das Bild aus dem Beispiel ab und kopiert es in den Ausgabepuffer. Der Abschnitt des Videos, der in den Ausgabepuffer kopiert wird, spiegelt das Quellrechteck wider, das über die [**IBasicVideo-Schnittstelle festgelegt**](/windows/desktop/api/Control/nn-control-ibasicvideo) wurde. Es spiegelt nicht das Zielrechteck wider.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




