---
description: Tritt auf, wenn ein Strich aus dem InkDisp-Objekt gelöscht wird.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: InkDisp. InkDeleted-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341183"
---
# <a name="inkdispinkdeleted-event"></a>InkDisp. InkDeleted-Ereignis

Tritt auf, wenn ein Strich aus dem [**InkDisp**](inkdisp-class.md) -Objekt gelöscht wird.

## <a name="syntax"></a>Syntax


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ in\]
</dt> <dd>

Gibt das ganzzahlige Array von Stroke ID-Informationen für alle Striche an, die bei Auftreten dieses Ereignisses gelöscht wurden.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das [**InkOverlay**](inkoverlay-class.md) -Objekt oder das [InkPicture](inkpicture-control-reference.md) -Steuerelement verwenden (wobei [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) auf " [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) " und " [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) " auf " [**strokeerase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)" festgelegt ist) und den Radierer über einen Strich übergeben, erhalten Sie die folgende Abfolge von Ereignissen:

-   **InkDeleted**
-   [**InkAdded**](inkdisp-inkadded.md)
-   **InkDeleted**

Die zusätzlichen [**InkAdded**](inkdisp-inkadded.md) -und **InkDeleted** -Ereignisse treten auf, da der zugrunde liegende Code einen internen, unsichtbaren Strich hinzufügt, um den Radierer zu verfolgen.

Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert. Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ieinkdeleted".

Das Ereignis **InkDeleted** wird auch dann ausgelöst, wenn Sie sich im Modus auswählen oder löschen befinden, nicht nur beim Einfügen von frei Hand Eingaben. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

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

[**InkAdded-Ereignis**](inkdisp-inkadded.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[InkPicture-Steuerelement Verweis](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

