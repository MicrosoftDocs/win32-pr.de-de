---
description: Tritt auf, wenn die inkrecognizercontext-Klasse Ergebnisse generiert hat, nachdem die backgrounderkennzewithalternativen-Methoden Methode aufgerufen wurde.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Inkrecognizercontext. erkentionwithalternativen-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216979"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>Inkrecognizercontext. erkentionwithalternativen-Ereignis

Tritt auf, wenn die [**inkrecognizercontext-Klasse**](inkrecognizercontext-class.md) Ergebnisse generiert hat, nachdem die [**backgrounderkennzewithalternativen-Methoden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) Methode aufgerufen wurde.

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

*Erkennungs Ergebnis* \[ in\]
</dt> <dd>

Das Erkennungs Ergebnis des Ereignisses.

</dd> <dt>

*CustomData* \[ in\]
</dt> <dd>

Die benutzerdefinierten Daten für das Erkennungs Ergebnis.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*Erkennungs Status* \[ in\]
</dt> <dd>

Der Erkennungs Status für das letzte Erkennungs Ergebnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Verhalten der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) ist unvorhersehbar, wenn Sie versuchen, vom Erkennungs Ereignishandler auf das ursprüngliche [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt zuzugreifen. Versuchen Sie nicht, dies zu tun. Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [**Erkennungs**](inkrecognizercontext-recognition.md) Ereignishandler fest. Anschließend können Sie dieses Flag Abfragen, um zu bestimmen, wann die **inkrecognizercontext** -Eigenschaften außerhalb des Ereignis Handlers geändert werden müssen.

Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert. Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID", " \_ unerecognitionwithalternativen".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inkrecognizercontext-Klasse**](inkrecognizercontext-class.md)
</dt> <dt>

[**Backgrounderkenzewithalternativen-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**Methode erkennen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Iinkrecognitionresult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

