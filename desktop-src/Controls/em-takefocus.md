---
title: EM_TAKEFOCUS Meldung (kommstrg. h)
description: Erzwingt, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des-Makros " \_ Take TakeFocus bearbeiten" senden.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Windows-Steuerelemente für EM_TAKEFOCUS Meldung
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
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476827"
---
# <a name="em_takefocus-message"></a>EM- \_ Fokus Meldung

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Erzwingt, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des-Makros [**" \_ Take TakeFocus bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) " senden.

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

Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird ignoriert, wenn das Bearbeitungs Steuerelement kein einzeilige Bearbeitungs Steuerelement ist.

Wenn das Bearbeitungs Steuerelement zuvor eine [**EM \_ nosetfocus**](em-nosetfocus.md) -Nachricht empfangen hat, scheint das Bearbeitungs Steuerelement den Fokus zu haben, ohne es tatsächlich zu haben. andernfalls erhält das Bearbeitungs Steuerelement den Fokus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**" \_ TakeFocus" Bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**EM \_ nosetfocus**](em-nosetfocus.md)
</dt> </dl>

 

 





