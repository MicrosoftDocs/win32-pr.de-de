---
description: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture. SelectionResized-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90e04533e3551fd4e1ba4ac661d8060377e6d06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360818"
---
# <a name="inkpictureselectionresized-event"></a>InkPicture. SelectionResized-Ereignis

Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.

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

Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionresized definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Bild-Steuerelement für Auswahl Eigenschaften \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**Inkrechteck-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

