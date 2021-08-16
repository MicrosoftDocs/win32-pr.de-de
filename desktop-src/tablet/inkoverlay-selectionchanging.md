---
description: Tritt ein, wenn sich die Auswahl der Freifläche im Steuerelement ändert, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: InkOverlay.SelectionChanging-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9b7fa52c4897c7e1152deff7636259e07e2768929223327243c2da0b59e362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218953"
---
# <a name="inkoverlayselectionchanging-event"></a>InkOverlay.SelectionChanging-Ereignis

Tritt ein, wenn sich die Auswahl der Freifläche im Steuerelement ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewSelection* \[ In\]
</dt> <dd>

Die neue Sammlung von [InkStrokes,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die ausgewählt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ \_ dispatch-only-Schnittstellen (dispinterfaces) von IInkOverlayEvents und IInkPictureEvents mit der ID DISPID \_ IOESelectionChanging definiert.

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

[**Selection-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

