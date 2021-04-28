---
description: 'InkCollector.Gesture-Ereignis: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.'
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: InkCollector.Gesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110188"
---
# <a name="inkcollectorgesture-event"></a>InkCollector.Gesture-Ereignis

Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.

## <a name="syntax"></a>Syntax


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Gestenereignis **generiert** hat.

</dd> <dt>

*Striche* \[ In\]
</dt> <dd>

Die [IInkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die von der -Erkannte als Geste zurückgegeben wurde.

</dd> <dt>

*Gesten* \[ In\]
</dt> <dd>

Ein Array von [**IInkGesture-Objekten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in der Reihenfolge der Konfidenz aus der -Erkannte.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn diese Geste abgebrochen werden soll; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEGesture definiert.

Wenn [**die CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des **Gestenereigniss** ein fester Wert, den Sie nicht programmgesteuert ändern können. Die Gestenerkennung ist im **InkAndGesture-Modus** schneller.

So verhindern Sie die Sammlung von Ink-Daten im [**InkAndGesture-Modus:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Legen [**Sie CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**InkAndGesture fest.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Löschen Sie den Strich im [**Stroke-Ereignis.**](inkcollector-stroke.md)
-   Verarbeiten Sie die Geste im **Gestenereignis.**

Um den Fluss von Ink während der Gesturierung zu verhindern, legen Sie [**die DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) auf **FALSE** fest.

Zusätzlich zum Einfügen von Ink wird das **Gestenereignis** im Auswahl- oder Löschmodus ausgelöst. Sie sind für die Nachverfolgung des Bearbeitungsmodus verantwortlich und sollten den Modus kennen, bevor Sie das Ereignis interpretieren.

> [!Note]  
> Um Gesten zu erkennen, müssen Sie ein Objekt oder Steuerelement verwenden, das Ink erfassen kann.

 

Anwendungsgesten werden als Gesten definiert, die in Ihrer Anwendung unterstützt werden.

Damit dieses Ereignis eintritt, muss das Objekt oder Steuerelement an einer Reihe von Anwendungsgesten interessiert sein. Um die Objekte oder Steuerelemente festzulegen, die für eine Reihe von Gesten von Interesse sind, rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) des Objekts oder Steuerelements auf.

Eine Liste der spezifischen Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

