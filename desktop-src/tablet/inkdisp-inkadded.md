---
description: Tritt ein, wenn dem InkDisp-Objekt ein Strich hinzugefügt wird.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: InkDisp.InkAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a6260660817d38795978371e99b241e3b5b2a88de2d9f2b6d3da678f117b522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939140"
---
# <a name="inkdispinkadded-event"></a>InkDisp.InkAdded-Ereignis

Tritt ein, wenn dem [**InkDisp-Objekt**](inkdisp-class.md) ein Strich hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ In\]
</dt> <dd>

Das ganzzahlige Array von Strich-ID-Informationen für alle Striche, die beim Auftreten dieses Ereignisses hinzugefügt wurden.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie das [**InkOverlay-Objekt**](inkoverlay-class.md) oder das [InkPicture-Steuerelement](inkpicture-control-reference.md) verwenden (wobei [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) [**gleich Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) und [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) gleich [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)ist) und den Radierer über einen Strich übergeben, erhalten Sie die folgende Sequenz von Ereignissen:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Die zusätzlichen Ereignisse **InkAdded** und [**InkDeleted**](inkdisp-inkdeleted.md) treten auf, da der zugrunde liegende Code einen internen, unsichtbaren Strich hinzufügt, um den Radierer nachzuverfolgen.

Diese Ereignismethode wird in der \_ IInkEvents-Schnittstelle definiert. Die \_ IInkEvents-Schnittstelle implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IEInkAdded.

Das **InkAdded-Ereignis** wird ausgelöst, auch wenn sie sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkDisp-Klasse**](inkdisp-class.md)
</dt> <dt>

[**EditingMode-Eigenschaft \[ inkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**EraserMode-Eigenschaft \[ inkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**InkDeleted-Ereignis**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[Referenz zum InkPicture-Steuerelement](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

