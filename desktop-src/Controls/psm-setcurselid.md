---
title: PSM_SETCURSELID-Nachricht (Prsht.h)
description: Aktiviert die angegebene Seite in einem Eigenschaftenblatt basierend auf dem Ressourcenbezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet-Makros SetCurSelByID senden.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877020"
---
# <a name="psm_setcurselid-message"></a>PSM \_ SETCURSELID-Nachricht

Aktiviert die angegebene Seite in einem Eigenschaftenblatt basierend auf dem Ressourcenbezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ressourcenbezeichner der zu aktivierenden Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das Fenster, in dem die Aktivierung verloren geht, empfängt den [PSN KILLACTIVE-Benachrichtigungscode, \_ ](psn-killactive.md) und das Fenster, in dem die Aktivierung erfolgt, empfängt den [PSN \_ SETACTIVE-Benachrichtigungscode.](psn-setactive.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





