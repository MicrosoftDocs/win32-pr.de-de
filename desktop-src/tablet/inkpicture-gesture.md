---
description: 'InkPicture.Gesture-Ereignis: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.'
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: InkPicture.Gesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c0307397fc5a197666894d40adce6f4a579e22d896df8df645b053580ee94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451067"
---
# <a name="inkpicturegesture-event"></a>InkPicture.Gesture-Ereignis

Tritt auf, wenn eine anwendungsspezifische *Geste* erkannt wird.

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

**VARIANT \_ TRUE,** wenn dieses Ereignis abgebrochen werden soll, z. B. um die Ink-Datei nicht zu löschen und das [**Stroke-Ereignis zu**](inkpicture-stroke.md) löschen. Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den **\_ Dispatch-Schnittstellen IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICEGesture definiert.

Wenn [**die CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des **Gestenereigniss** ein fester Wert, den Sie nicht programmgesteuert ändern können. Die Gestenerkennung ist im **InkAndGesture-Modus** schneller.

So verhindern Sie die Sammlung von Ink-Daten im [**InkAndGesture-Modus:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   Legen [**Sie CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) auf [**InkAndGesture fest.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)
-   Löschen Sie den Strich im [**Stroke-Ereignis.**](inkpicture-stroke.md)
-   Verarbeiten Sie die Geste im **Gestenereignis.**

Um den Fluss von Ink während der Gestur zu verhindern, legen Sie [**die DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) auf **FALSE fest.**

Zusätzlich zum Einfügen von Ink wird das **Gestenereignis** ausgelöst, wenn sich der Auswahl- oder Löschmodus befindet. Sie sind für die Nachverfolgung des Bearbeitungsmodus verantwortlich und sollten den Modus kennen, bevor Sie das Ereignis interpretieren.

> [!Note]  
> Um Gesten zu erkennen, müssen Sie ein Objekt oder Steuerelement verwenden, das Ink sammeln kann.

 

Anwendungsgesten werden als Gesten definiert, die in Ihrer Anwendung unterstützt werden.

Damit dieses Ereignis eintritt, muss das Objekt oder Steuerelement interesse an einer Reihe von Anwendungsgesten haben. Rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) des Objekts oder Steuerelements auf, um die Objekte oder Steuerelemente für eine Reihe von Gesten zu verwenden.

Eine Liste mit bestimmten Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

