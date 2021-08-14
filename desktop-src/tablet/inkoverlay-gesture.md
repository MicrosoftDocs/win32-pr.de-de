---
description: 'InkOverlay.Gesture-Ereignis: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.'
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: InkOverlay.Gesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01689465e9951a5b8cd6548cabb0be4a0bde32c7cf46c2ea4c71b3bb38151eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219311"
---
# <a name="inkoverlaygesture-event"></a>InkOverlay.Gesture-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Gestenereignis [**generiert**](inkcollector-gesture.md) hat.

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

Gibt an, ob die Auflistung dieser Geste abgebrochen werden soll, z. B. nicht, um die Ink-Datei zu löschen und das [**Stroke-Ereignis zu**](inkcollector-stroke.md) löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEGesture definiert.

Wenn [**die CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des [**Gestenereigniss**](inkcollector-gesture.md) ein fester Wert, den Sie nicht programmgesteuert ändern können. Die Gestenerkennung ist im **InkAndGesture-Modus** schneller.

So verhindern Sie die Sammlung von Ink-Daten im [**InkAndGesture-Modus:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Legen [**Sie CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**InkAndGesture fest.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Löschen Sie den Strich im [**Stroke-Ereignis.**](inkcollector-stroke.md)
-   Verarbeiten Sie die Geste im [**Gestenereignis.**](inkcollector-gesture.md)

Um den Fluss von Ink während der Gestur zu verhindern, legen Sie [**die DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) auf **FALSE fest.**

Zusätzlich zum Einfügen von Ink wird das [**Gestenereignis**](inkcollector-gesture.md) ausgelöst, wenn sich der Auswahl- oder Löschmodus befindet. Sie sind für die Nachverfolgung des Bearbeitungsmodus verantwortlich und sollten den Modus beachten, bevor Sie das Ereignis interpretieren.

> [!Note]  
> Um Gesten zu erkennen, müssen Sie ein Objekt oder Steuerelement verwenden, das Ink sammeln kann.

 

Anwendungsgesten werden als Gesten definiert, die in Ihrer Anwendung unterstützt werden.

Damit dieses Ereignis eintritt, muss das Objekt oder Steuerelement interesse an einer Reihe von Anwendungsgesten haben. Rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) des Objekts oder Steuerelements auf, um die Objekte oder Steuerelemente für eine Reihe von Gesten zu verwenden.

Eine Liste mit bestimmten Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

