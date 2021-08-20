---
description: Tritt ein, wenn die InkRecognizerContext-Klasse nach dem Aufruf der BackgroundRecognizeWithAlternates-Methode Ergebnisse generiert hat.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: InkRecognizerContext.RecognitionWithAlternates-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a693e3f13abb92f0d486d419bc5cf02d214d50204e4c64c4e3148d2b400c9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041920"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>InkRecognizerContext.RecognitionWithAlternates-Ereignis

Tritt ein, wenn die [**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md) nach dem Aufruf der [**BackgroundRecognizeWithAlternates-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) Ergebnisse generiert hat.

## <a name="syntax"></a>Syntax


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RecognitionResult* \[ In\]
</dt> <dd>

Das Erkennungsergebnis des Ereignisses.

</dd> <dt>

*CustomData* \[ In\]
</dt> <dd>

Die benutzerdefinierten Daten für das Erkennungsergebnis.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> <dt>

*RecognitionStatus* \[ In\]
</dt> <dd>

Der Erkennungsstatus ab dem letzten Erkennungsergebnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Verhalten der Anwendungsprogrammierschnittstelle (API) ist unvorhersehbar, wenn Sie versuchen, über den Erkennungsereignishandler Zugriff auf das ursprüngliche [**InkRecognizerContext-Objekt**](inkrecognizercontext-class.md) zu erhalten. Versuchen Sie nicht, dies zu tun. Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [**Erkennungsereignishandler**](inkrecognizercontext-recognition.md) fest. Anschließend können Sie dieses Flag abrufen, um zu bestimmen, wann die **InkRecognizerContext-Eigenschaften** außerhalb des Ereignishandlers geändert werden sollten.

Diese Ereignismethode wird in der \_ IInkEvents-Schnittstelle definiert. Die \_ IInkEvents-Schnittstelle implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IRERecognitionWithAlternates.

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

[**BackgroundRecognizeWithAlternates-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Recognize-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**IInkRecognitionResult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

