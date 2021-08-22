---
title: EM_TAKEFOCUS Meldung (Commctrl.h)
description: Erzwingt, dass ein einzeiliges Bearbeitungssteuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des \_ TakeFocus-Makros bearbeiten senden.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8283f2f9ea033439ef9ad7ec0ce40b08bb6396db8f5ebc7a9b1d513f29c209a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437140"
---
# <a name="em_takefocus-message"></a>EM \_ TAKEFOCUS-Nachricht

\[Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird in zukünftigen Versionen von Windows möglicherweise nicht mehr unterstützt.\]

Erzwingt, dass ein einzeiliges Bearbeitungssteuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des [**\_ TakeFocus-Makros bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) senden.

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

Diese Meldung wird ignoriert, wenn das Bearbeitungssteuerelement kein einzeiliges Bearbeitungssteuerelement ist.

Wenn das Bearbeitungssteuerelement zuvor eine [**EM \_ NOSETFOCUS-Meldung**](em-nosetfocus.md) empfangen hat, scheint das Bearbeitungssteuerelement den Fokus zu haben, ohne ihn tatsächlich zu haben. Andernfalls erhält das Bearbeitungssteuerelement den Fokus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**Bearbeiten von \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**EM \_ NOSETFOCUS**](em-nosetfocus.md)
</dt> </dl>

 

 





