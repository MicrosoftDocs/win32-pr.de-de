---
title: TCM_SETCURFOCUS Meldung (kommstrg. h)
description: Legt den Fokus auf eine angegebene Registerkarte in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setcurrfocus-Makros senden.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Windows-Steuerelemente für TCM_SETCURFOCUS Meldung
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956497"
---
# <a name="tcm_setcurfocus-message"></a>TCM- \_ setcurrfocus-Nachricht

Legt den Fokus auf eine angegebene Registerkarte in einem Registerkarten-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setcurrfocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index der Registerkarte, die den Fokus erhält.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn das Registerkarten-Steuerelement den [**TCS \_ -Schalt**](tab-control-styles.md) Flächen Stil (Schaltflächen Modus) aufweist, kann sich die Registerkarte mit dem Fokus von der ausgewählten Registerkarte unterscheiden. Wenn z. b. eine Registerkarte ausgewählt ist, kann der Benutzer die Pfeiltasten drücken, um den Fokus auf eine andere Registerkarte festzulegen, ohne die ausgewählte Registerkarte zu ändern. Im Schaltflächen Modus legt **TCM \_ setcurrfocus** den Eingabefokus auf die Schaltfläche fest, die der angegebenen Registerkarte zugeordnet ist, aber die ausgewählte Registerkarte wird nicht geändert.

Wenn das Registerkarten-Steuerelement nicht über die [**TCS- \_ Schalt**](tab-control-styles.md) Flächen verfügt, wird durch das Ändern des Fokus auch die ausgewählte Registerkarte geändert. In diesem Fall sendet das Registerkarten-Steuer [Element die TCN \_ selchanging](tcn-selchanging.md) -und [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Codes an das übergeordnete Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TCM \_ getcurrfocus**](tcm-getcurfocus.md)
</dt> </dl>

 

 





