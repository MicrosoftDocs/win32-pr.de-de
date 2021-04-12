---
description: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der Selection-Eigenschaft.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: InkOverlay. selectionverschodas Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348668"
---
# <a name="inkoverlayselectionmoved-event"></a>InkOverlay. selectionverschodas Ereignis

Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und einfügeprozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Oldselectionrect* \[ in\]
</dt> <dd>

Das umschließende Rechteck der ausgewählten [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, wie es vor dem Auslösen des **selectionverschochereignisses** vorhanden war.

> [!Note]  
> Dieses Rechteck wird in Freihand Raumkoordinaten angegeben, die rückgängig-Szenarien ermöglichen.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

TDiese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionverschot definiert.

Zum Abrufen des neuen umgebenden Rechtecks der Auflistung von Strichen, die verschoben wurden, müssen Sie die [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) -Methode aufrufen.

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

 

