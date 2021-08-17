---
title: EM_NOSETFOCUS (Commctrl.h)
description: Verhindert, dass ein einzeilenbasiertes Bearbeitungssteuer steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des Makros \_ Edit NoSetFocus senden.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS der Windows Steuerelemente
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ac35a30ff3deac7e9d6d227a6e8c403e6096e272ea89067dd817add9b2426e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831193"
---
# <a name="em_nosetfocus-message"></a>EM \_ NOSETFOCUS-Meldung

\[Für die interne Verwendung vorgesehen; wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird in zukünftigen Versionen des -Windows.\]

Verhindert, dass ein einzeilenbasiertes Bearbeitungssteuer steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des Makros [**\_ Edit NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.

## <a name="remarks"></a>Hinweise

Diese Meldung wird ignoriert, wenn das Bearbeitungssteuer steuerelement kein einzeilenbasiertes Bearbeitungssteuer steuerelement ist.

Nachdem diese Nachricht gesendet wurde, ist die Auswirkung dauerhaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Bearbeiten \_ von NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ TAKEFOCUS**](em-takefocus.md)
</dt> </dl>

 

 





