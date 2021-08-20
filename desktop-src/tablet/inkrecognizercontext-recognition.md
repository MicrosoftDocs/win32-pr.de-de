---
description: Tritt ein, wenn der InkRecognizerContext Ergebnisse aus der BackgroundRecognize-Methode generiert hat.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: InkRecognizerContext.Recognition-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f6c4799f3366003d14451a19a7bea19ea35aadcce9226f25f1fe80a14ab19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966939"
---
# <a name="inkrecognizercontextrecognition-event"></a>InkRecognizerContext.Recognition-Ereignis

Tritt ein, wenn [**der InkRecognizerContext**](inkrecognizercontext-class.md) Ergebnisse aus der [**BackgroundRecognize-Methode generiert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) hat.

## <a name="syntax"></a>Syntax


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RecognizedString* \[ In\]
</dt> <dd>

Der Text des Erkennungsergebnis mit der höchsten Konfidenz.

Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> <dt>

*CustomData* \[ In\]
</dt> <dd>

Das -Objekt, das die benutzerdefinierten Daten für das Erkennungsergebnis enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> <dt>

*RecognitionStatus* \[ In\]
</dt> <dd>

Der Erkennungsstatus ab dem letzten Erkennungsergebnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Verhalten der Anwendungsprogrammierschnittstelle (API) ist unvorhersehbar, wenn Sie versuchen, über den Erkennungsereignishandler Zugriff auf das ursprüngliche [**InkRecognizerContext-Objekt**](inkrecognizercontext-class.md) zu erhalten. Versuchen Sie nicht, dies zu tun. Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [Erkennungsereignishandler](ink-recognition.md) fest. Anschließend können Sie dieses Flag abrufen, um zu bestimmen, wann die **InkRecognizerContext-Eigenschaften** außerhalb des Ereignishandlers geändert werden sollten.

Diese Ereignismethode wird in der \_ IInkEvents-Schnittstelle definiert. Die \_ IInkEvents-Schnittstelle implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IRERecognition.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md)
</dt> <dt>

[**BackgroundRecognize-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**InkRecognitionStatus-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Recognize-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**IInkRecognitionResult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

