---
title: EM_NOSETFOCUS Meldung (kommstrg. h)
description: Verhindert, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des " \_ nosetfocus"-Makros bearbeiten senden.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Windows-Steuerelemente für EM_NOSETFOCUS Meldung
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
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105104"
---
# <a name="em_nosetfocus-message"></a>EM \_ nosetfocus-Nachricht

\[Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen. Diese Meldung wird möglicherweise in zukünftigen Versionen von Windows nicht mehr unterstützt.\]

Verhindert, dass ein einzeilige Bearbeitungs Steuerelement den Tastaturfokus erhält. Sie können diese Nachricht explizit oder mithilfe des " [**\_ nosetfocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) "-Makros bearbeiten senden.

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

Nachdem diese Nachricht gesendet wurde, ist der Effekt permanent.

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

[**\_Nosetfocus bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM- \_ Fokus**](em-takefocus.md)
</dt> </dl>

 

 





