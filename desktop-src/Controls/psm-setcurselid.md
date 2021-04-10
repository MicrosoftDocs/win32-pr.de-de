---
title: PSM_SETCURSELID Meldung (prsht. h)
description: Aktiviert die angegebene Seite in einem Eigenschaften Blatt basierend auf dem Ressourcen Bezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setcurrselbyid senden.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Windows-Steuerelemente für PSM_SETCURSELID Meldung
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
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105086"
---
# <a name="psm_setcurselid-message"></a>PSM- \_ setcurrselid-Nachricht

Aktiviert die angegebene Seite in einem Eigenschaften Blatt basierend auf dem Ressourcen Bezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrselbyid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Ressourcen Bezeichner der zu aktivierenden Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Fenster, das die Aktivierung verliert, empfängt den [PSN- \_ killactive](psn-killactive.md) -Benachrichtigungs Code, und das Fenster, das die Aktivierung erlangt, empfängt den [PSN- \_ SETACTIVE](psn-setactive.md) -Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





