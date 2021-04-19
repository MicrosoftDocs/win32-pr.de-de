---
description: Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die Selection-Eigenschaft
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: InkOverlay. SelectionChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366173"
---
# <a name="inkoverlayselectionchanged-event"></a>InkOverlay. SelectionChanged-Ereignis

Tritt auf, wenn sich die Auswahl von frei Hand Eingaben innerhalb des-Steuer Elements geändert hat, z. b. durch Änderungen an der Benutzeroberfläche, Ausschneide-und Einfüge Prozeduren oder die [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) -Eigenschaft

## <a name="syntax"></a>Syntax


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Es sind keine Ereignisdaten vorhanden.

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioeselectionchanged definiert.

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

 

 




