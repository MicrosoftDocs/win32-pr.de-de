---
description: Die Transform-Methode transformiert ein Eingabe Beispiel, um ein Ausgabe Beispiel zu erhalten.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Ctransformfilter. Transform-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351263"
---
# <a name="ctransformfiltertransform-method"></a>Ctransformfilter. Transform-Methode

Die- `Transform` Methode transformiert ein Eingabe Beispiel, um ein Ausgabe Beispiel zu erhalten.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*kehren* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle der Eingabe Stichprobe.

</dd> <dt>

*Schmollmund* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Ausgabe Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklasse gibt "E unerwartete" zurück \_ .

Die abgeleitete Klasse sollte einen **HRESULT** -Wert zurückgeben, der den Erfolg oder Misserfolg angibt. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Stellen Sie dieses Beispiel nicht bereit.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, um Ausgabedaten zu entwickeln. Lesen Sie die Eingabedaten aus dem im *pIn* -Parameter angegebenen Beispiel, und schreiben Sie die neuen Daten in das durch den *Pout* -Parameter angegebene Beispiel.

Bevor der Filter diese Methode aufruft, werden die Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert. Die- `Transform` Methode sollte alle Eigenschaften festlegen, die sich zwischen den beiden Beispielen unterscheiden, mithilfe von **imediasample** -Methoden oder der [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle (falls verfügbar).

Wenn der Filter dieses Beispiel nicht bereitstellt (z. b. zur Unterstützung der Qualitätskontrolle), sollte die Methode den Wert S false zurückgeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




