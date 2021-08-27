---
description: Weist ein Fenster zum Löschen von Images an, das mit neuen DROPDESCRIPTION-Informationen aktualisiert werden soll.
title: DDWM_UPDATEWINDOW Meldung
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032838"
---
# <a name="ddwm_updatewindow-message"></a>DDWM \_ UPDATEWINDOW-Nachricht

Weist ein Fenster zum Löschen von Images an, das mit neuen [**DROPDESCRIPTION-Informationen**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) aktualisiert werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

DDWM \_ UPDATEWINDOW ist als WM \_ USER+3 definiert.

Wenn sich der Zustand eines Ablagevorgangs ändert , z. B. als Reaktion auf einen Modifiziererschlüssel, gibt [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) einen neuen [**DROPEFFECT-Wert**](../com/dropeffect-constants.md) zurück (dieser **DROPEFFECT-Wert** kann auch über [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)empfangen werden). Als Reaktion aktualisiert die Anwendung die [**DROPDESCRIPTION-Struktur**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) des Ablageziels mit einem neuen [**DROPIMAGETYPE-Wert,**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) der die auf das Visual des Ziehfensters anzuwendende Dekoration angibt. Beispielsweise ein Hinweis darauf, dass die Datei kopiert statt verschoben wird oder dass das Objekt nicht an diesem Speicherort abgelegt werden kann. Die Visuals werden jedoch erst aktualisiert, wenn das Objekt eine **DDWM \_ UPDATEWINDOW-Meldung** empfängt.

Das [DragWindow-Zwischenablageformat](clipboard.md) stellt das **HWND** des Empfänger-Ziehfensters an den Absender der **DDWM \_ UPDATEWINDOW-Nachricht** bereit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 
