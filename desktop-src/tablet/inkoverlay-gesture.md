---
description: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: InkOverlay. Gesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3db800db2d1fca9ee1b00620c698a592ac2121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351066"
---
# <a name="inkoverlaygesture-event"></a>InkOverlay. Gesten-Ereignis

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

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**Gesten**](inkcollector-gesture.md) Ereignis generiert hat.

</dd> <dt>

*Striche* \[ in\]
</dt> <dd>

Die [iinkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die die Erkennung als Geste zurückgegeben hat.

</dd> <dt>

*Gesten* \[ in\]
</dt> <dd>

Ein Array von [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekten, in der Reihenfolge der Sicherheit, von der Erkennung.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob die Auflistung dieser Geste abgebrochen werden soll, z. b. nicht, um die frei Hand Eingabe zu löschen und das [**Stroke**](inkcollector-stroke.md) -Ereignis auszulösen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icegesten definiert.

Wenn die [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) -Eigenschaft auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des [**Gesten**](inkcollector-gesture.md) Ereignisses ein fester Wert, den Sie nicht Programm gesteuert ändern können. Die Gestenerkennung ist schneller im **inkandgesten** -Modus.

So verhindern Sie die Sammlung von frei Hand Eingaben im [**inkandgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Modus:

-   Legen Sie [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**inkandgeste**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)fest.
-   Löschen Sie den Strich im [**Stroke**](inkcollector-stroke.md) -Ereignis.
-   Verarbeiten Sie die Geste im [**Gesten**](inkcollector-gesture.md) Ereignis.

Legen Sie die [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) -Eigenschaft auf **false** fest, um den Fluss von frei Hand Eingaben zu verhindern.

Zusätzlich zum Einfügen von frei Hand Eingaben wird das [**Gesten**](inkcollector-gesture.md) Ereignis ausgelöst, wenn Sie sich im SELECT-oder Erase-Modus befinden. Sie sind verantwortlich für die Nachverfolgung des Bearbeitungsmodus und sollten den Modus vor der Interpretation des Ereignisses beachten.

> [!Note]  
> Um Gesten zu erkennen, müssen Sie ein Objekt oder ein Steuerelement verwenden, das frei Hand Eingaben erfassen kann.

 

Anwendungs Gesten werden als Gesten definiert, die in der Anwendung unterstützt werden.

Damit dieses Ereignis auftritt, muss das Objekt oder Steuerelement für eine Reihe von Anwendungs Gesten von Interesse sein. Um die Objekte oder Steuerelemente festzulegen, die für einen Satz von Gesten relevant sind, müssen Sie die [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) -Methode des Objekts oder Steuer Elements aufrufen.

Eine Liste der spezifischen Anwendungs Gesten finden Sie unter dem [**Enumerationstyp inkapplicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Inkapplicationgesten-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

