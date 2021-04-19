---
description: Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der Selection-Eigenschaft.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: InkOverlay. SelectionChanging-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364173"
---
# <a name="inkoverlayselectionchanging-event"></a>InkOverlay. SelectionChanging-Ereignis

Tritt auf, wenn die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert wird, z. b. durch Änderungen an der Benutzeroberfläche, von Ausschneide-und Einfüge Prozeduren oder von der [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Neuauswahl* \[ in\]
</dt> <dd>

Die neue Sammlung von [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , die ausgewählt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID "DISPID \_ ioeselectionchanging" definiert.

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
</dt> </dl>

 

