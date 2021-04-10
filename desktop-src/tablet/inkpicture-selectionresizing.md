---
description: Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture. selectionresisierungsereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960669"
---
# <a name="inkpictureselectionresizing-event"></a>InkPicture. selectionresierend-Ereignis

Tritt ein, wenn die Größe der aktuellen Auswahl geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und-Einfügen-Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) -Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das umgebende Rechteck der Auswahl nach dem **selectionresiup** -Ereignis.

> [!Note]  
> Dieses Rechteck wird in Client Fenster Koordinaten angegeben, das Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioeselectionresiup definiert.

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

 

 




