---
description: 'Tritt auf, wenn das InkEdit-Steuerelement Ergebnisse manuell von einem Rückruf der InkEdit:: Recognition-Methode oder automatisch nach dem Auslösen des Erkennungs Timeouts abruft.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: InkEdit. erkentionresult-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218053"
---
# <a name="inkeditrecognitionresult-event"></a>InkEdit. erkentionresult-Ereignis

Tritt auf, wenn das [InkEdit](inkedit-control-reference.md) -Steuerelement Ergebnisse manuell von einem Rückruf der [**InkEdit::**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) Recognition-Methode oder automatisch nach dem Auslösen des Erkennungs Timeouts abruft.

## <a name="syntax"></a>Syntax


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Erkennungs Ergebnis* \[ in\]
</dt> <dd>

Ein [**iinkrecognitionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt, das das Ergebnis der Erkennung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieerecognitionresult.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Methode " \[ InkEdit-Steuerelement" erkennen\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

