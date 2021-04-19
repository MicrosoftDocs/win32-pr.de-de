---
description: Tritt auf, wenn der inkrecognizercontext Ergebnisse aus der backgrounderkennmethode generiert hat.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Inkrecognizercontext. Recognition-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350059"
---
# <a name="inkrecognizercontextrecognition-event"></a>Inkrecognizercontext. Recognition-Ereignis

Tritt auf, wenn der [**inkrecognizercontext**](inkrecognizercontext-class.md) Ergebnisse aus der [**backgrounderkennmethode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) generiert hat.

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

*Erkennungs Zeichenfolge* \[ in\]
</dt> <dd>

Der Erkennungs Ergebnis Text mit dem höchsten Vertrauen.

Weitere Informationen zum BSTR-Datentyp finden [Sie unter Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ in\]
</dt> <dd>

Das-Objekt, das die benutzerdefinierten Daten für das Erkennungs Ergebnis enthält.

Weitere Informationen zur VARIANT-Struktur finden [Sie unter Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*Erkennungs Status* \[ in\]
</dt> <dd>

Der Erkennungs Status für das letzte Erkennungs Ergebnis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Verhalten der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) ist unvorhersehbar, wenn Sie versuchen, vom Erkennungs Ereignishandler auf das ursprüngliche [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt zuzugreifen. Versuchen Sie nicht, dies zu tun. Wenn Sie dies tun müssen, erstellen Sie stattdessen ein Flag, und legen Sie es im [Erkennungs](ink-recognition.md) Ereignishandler fest. Anschließend können Sie dieses Flag Abfragen, um zu bestimmen, wann die **inkrecognizercontext** -Eigenschaften außerhalb des Ereignis Handlers geändert werden müssen.

Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert. Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ unerekognition".

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

[**Backgrounderkenungsmethode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Inkrecognitionstatus-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Methode erkennen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Iinkrecognitionresult-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

