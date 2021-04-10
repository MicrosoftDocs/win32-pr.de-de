---
description: Tritt auf, wenn dem InkDisp-Objekt ein Strich hinzugefügt wird.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: InkDisp. InkAdded-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041703"
---
# <a name="inkdispinkadded-event"></a>InkDisp. InkAdded-Ereignis

Tritt auf, wenn dem [**InkDisp**](inkdisp-class.md) -Objekt ein Strich hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ in\]
</dt> <dd>

Das ganzzahlige Array von Stroke ID-Informationen für alle Striche, die beim Eintreten dieses Ereignisses hinzugefügt wurden.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das [**InkOverlay**](inkoverlay-class.md) -Objekt oder das [InkPicture](inkpicture-control-reference.md) -Steuerelement verwenden (wobei [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) auf " [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) " und " [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) " auf " [**strokeerase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)" festgelegt ist) und den Radierer über einen Strich übergeben, erhalten Sie die folgende Abfolge von Ereignissen:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Die zusätzlichen **InkAdded** -und [**InkDeleted**](inkdisp-inkdeleted.md) -Ereignisse treten auf, da der zugrunde liegende Code einen internen, unsichtbaren Strich hinzufügt, um den Radierer zu verfolgen.

Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert. Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ieinkadded".

Das **InkAdded** -Ereignis wird auch dann ausgelöst, wenn der Modus zum auswählen oder Löschen nicht nur beim Einfügen von frei Hand Eingaben vorliegt. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**EditingMode-Eigenschaft \[ InkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**EraserMode-Eigenschaft ( \[ InkOverlay-Klasse)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**InkDeleted-Ereignis**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[InkPicture-Steuerelement Verweis](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

