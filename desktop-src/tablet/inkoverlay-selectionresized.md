---
description: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: InkOverlay. SelectionResized-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218047"
---
# <a name="inkoverlayselectionresized-event"></a>InkOverlay. SelectionResized-Ereignis

Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Oldselectionrect* \[ in\]
</dt> <dd>

Das umgebende Rechteck der ausgewählten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, wie es vorhanden war, bevor das **SelectionResized** -Ereignis ausgelöst wurde.

> [!Note]  
> Dieses Rechteck wird in Freihand Raumkoordinaten angegeben, die rückgängig-Szenarien ermöglichen.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionresized definiert.

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

[**Auswahl Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**Inkrechteck-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

