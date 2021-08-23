---
title: LB_SETLOCALE (Winuser.h)
description: Legt das aktuelle Locale des Listenfelds fest. Sie können das -Locale verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem LBS SORT-Format) und des von der \_ LB ADDSTRING-Meldung hinzugefügten Texts \_ zu bestimmen.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE der Windows Steuerelemente
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
ms.openlocfilehash: 623b8550b3d5f382ddc8ccc1e1cfcf861a2f8c0a7877ba60c57e393abc1401d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958539"
---
# <a name="lb_setlocale-message"></a>LB \_ SETLOCALE-Meldung

Legt das aktuelle Locale des Listenfelds fest. Sie können das -Locale verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit [**dem LBS \_ SORT-Format)**](list-box-styles.md) und des von der [**LB \_ ADDSTRING-Meldung**](lb-addstring.md) hinzugefügten Texts zu bestimmen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Locale Identifier an, den das Listenfeld beim Hinzufügen von Text zum Sortieren verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Locale Identifier. Wenn der *wParam-Parameter* ein auf dem System nicht installiertes Locale angibt, ist der Rückgabewert LB ERR, und das aktuelle Listenfeld-Locale \_ wird nicht geändert.

## <a name="remarks"></a>Hinweise

Verwenden Sie das [**MAKELCID-Makro,**](/windows/desktop/api/winnt/nf-winnt-makelcid) um einen Locale Identifier zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETLOCALE**](lb-getlocale.md)
</dt> </dl>

 

