---
title: EN_ALIGN_RTL_EC Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer die Bearbeitungssteuerungsrichtung von rechts nach links geändert hat. Das übergeordnete Fenster des Bearbeitungssteuer elements empfängt diesen Benachrichtigungscode über eine WM \_ COMMAND-Meldung.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437090"
---
# <a name="en_align_rtl_ec-notification-code"></a>EN ALIGN RTL EC notification code (EN \_ ALIGN \_ RTL \_ EC-Benachrichtigungscode)

Wird gesendet, wenn der Benutzer die Bearbeitungssteuerungsrichtung von rechts nach links geändert hat. Das übergeordnete Fenster des Bearbeitungssteuer elements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des Bearbeitungssteuerzeichens. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungssteuer steuerelement, das den Benachrichtigungscode sendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn auf Ihrem System eine bidirektionale Sprache installiert ist, z. B. Arabisch oder Hebräisch, können Sie die Bearbeitungssteuerungsrichtung ändern, indem Sie STRG+LSHIFT (für von links nach rechts) und STRG+RSHIFT (für von rechts nach links) verwenden.

**Umfangreiche Bearbeitung:** Dieser Benachrichtigungscode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

