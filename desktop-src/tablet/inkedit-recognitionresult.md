---
description: Tritt ein, wenn das InkEdit-Steuerelement manuell Ergebnisse aus einem Aufruf der InkEdit::Recognize-Methode abruft oder automatisch nach dem Ausgelösten Erkennungstimeout.
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: InkEdit.RecognitionResult-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef71d38be31f32c59919a9ce4f24fd90b2d188d86a26e81821f6f7987da31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939080"
---
# <a name="inkeditrecognitionresult-event"></a>InkEdit.RecognitionResult-Ereignis

Tritt ein, wenn das [InkEdit-Steuerelement](inkedit-control-reference.md) manuell Ergebnisse aus einem Aufruf der [**InkEdit::Recognize-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) abruft oder automatisch nach dem Ausgelösten Erkennungstimeout.

## <a name="syntax"></a>Syntax


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RecognitionResult* \[ In\]
</dt> <dd>

Ein [**IInkRecognitionResult-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) das das Ergebnis der Erkennung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IeeRecognitionResult.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**Recognize Method \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

