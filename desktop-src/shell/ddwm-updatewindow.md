---
description: Weist ein Fenster zum Löschen von Bildern an, das mithilfe neuer dropdescription-Informationen aktualisiert werden soll.
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
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977312"
---
# <a name="ddwm_updatewindow-message"></a>Ddwm- \_ UpdateWindow-Meldung

Weist ein Fenster zum Löschen von Bildern an, das mithilfe neuer [**dropdescription**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) -Informationen aktualisiert werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ddwm \_ UpdateWindow ist als WM- \_ Benutzer + 3 definiert.

Wenn sich der Zustand eines Drop-Vorgangs ändert – z. b. als Reaktion auf einen modifiziererschlüssel – gibt [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) einen neuen [**DropEffect**](../com/dropeffect-constants.md) -Wert zurück (dieser **DropEffect** -Wert kann auch über [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)empfangen werden). In der Antwort aktualisiert die Anwendung die [**dropdescription**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) -Struktur des Ablage Ziels mit einem neuen [**dropimagetype**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) -Wert, der die Dekoration angibt, die auf die Visualisierung des Zieh Fensters angewendet werden soll. beispielsweise ein Hinweis darauf, dass die Datei kopiert wird, anstatt verschoben zu werden, oder dass das Objekt an diesem Speicherort nicht gelöscht werden kann. Die visuellen Elemente werden jedoch erst aktualisiert, wenn das Objekt eine **ddwm \_ UpdateWindow** -Meldung empfängt.

Das [dragwindow](clipboard.md) -Zwischenablage Format gibt das **HWND** des Empfänger Zieh Fensters an den Absender der **ddwm \_ UpdateWindow** -Nachricht an.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 
