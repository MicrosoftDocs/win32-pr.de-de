---
title: PSM_SETCURSEL Meldung (prsht. h)
description: Aktiviert die angegebene Seite in einem Eigenschaften Blatt. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setcurrsel senden.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Windows-Steuerelemente für PSM_SETCURSEL Meldung
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103470"
---
# <a name="psm_setcursel-message"></a>PSM- \_ setcurrsel-Nachricht

Aktiviert die angegebene Seite in einem Eigenschaften Blatt. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrsel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Seite. Eine Anwendung kann den Index oder das Handle oder beides angeben. Wenn beide angegeben sind, hat *LPARAM* Vorrang.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Handle für die zu Aktivier elnde Seite. Eine Anwendung kann den Index oder das Handle oder beides angeben. Wenn beide angegeben sind, hat *LPARAM* Vorrang.

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



 

 





