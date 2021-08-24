---
title: HDM_SETHOTDIVIDER (Commctrl.h)
description: Ändert die Farbe eines Unterteilers zwischen Headerelementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben. Sie können diese Nachricht explizit senden oder das \_ Header-SetHotDivider-Makro verwenden.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedfca7a6f0d10651984efb63c4db63116c4a53d2b9f9b85905c93fc12e6ca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544750"
---
# <a name="hdm_sethotdivider-message"></a>HDM \_ SETHOTDIVIDER-Nachricht

Ändert die Farbe eines Unterteilers zwischen Headerelementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben. Sie können diese Nachricht explizit senden oder das [**\_ Header-SetHotDivider-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des Werts, der *durch lParam dargestellt wird.* Die folgenden Werte sind möglich:



| Wert                                                                                                                                    | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE!</dt> </dl>    | Gibt *an, dass lParam* die Clientkoordinaten des Zeigers enthält.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE!</dt> </dl> | Gibt an, *dass lParam* einen Divisionsindexwert enthält.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein in *lParam gehaltener* Wert wird abhängig vom Wert von *wParam interpretiert.*

Wenn *wParam* **TRUE ist,** stellt *lParam* die x- und y-Koordinaten des Zeigers dar. Die x-Koordinate befindet sich im unteren Wort, und die y-Koordinate befindet sich im hohen Wort. Wenn das Headersteuerteiler die Nachricht empfängt, hebt es den entsprechenden Unterteiler basierend auf den *lParam-Koordinaten* hervor.

Wenn *wParam* **FALSE ist,** *stellt lParam* den ganzzahligen Index des zu hervorgehobenen Unterteilers dar.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der dem Index des Unterteilers entspricht, den das Steuerelement hervorgehoben hat.

## <a name="remarks"></a>Hinweise

Diese Meldung erstellt einen Effekt, der von einem Headersteuersatz automatisch erzeugt wird, wenn es den [**\_ HDS-DRAGDROP-Stil**](header-control-styles.md) auft. The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





