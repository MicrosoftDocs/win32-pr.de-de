---
title: LB_SETLOCALE Meldung (Winuser. h)
description: Legt das aktuelle Gebiets Schema des Listen Felds fest. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem lbs \_ -Sortier Stil) und des von der LB AddString-Nachricht hinzugefügten Texts zu bestimmen \_ .
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Windows-Steuerelemente für LB_SETLOCALE Meldung
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040892"
---
# <a name="lb_setlocale-message"></a>SLB- \_ setlocale-Meldung

Legt das aktuelle Gebiets Schema des Listen Felds fest. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil) und des von der [**lb \_ AddString**](lb-addstring.md) -Nachricht hinzugefügten Texts zu bestimmen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Gebiets Schema Bezeichner an, der beim Hinzufügen von Text vom Listenfeld zum Sortieren verwendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Gebiets Schema Bezeichner. Wenn der *wParam* -Parameter ein Gebiets Schema angibt, das nicht auf dem System installiert ist, lautet der Rückgabewert "lb err", \_ und das aktuelle Listenfeld "locale" wird nicht geändert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) -Makro zum Erstellen eines Gebiets Schema Bezeichners.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB \_ getLocale**](lb-getlocale.md)
</dt> </dl>

 

