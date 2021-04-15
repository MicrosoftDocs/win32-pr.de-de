---
title: CB_SETLOCALE Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB- \_ setlocale-Nachricht, um das aktuelle Gebiets Schema des Kombinations Felds festzulegen. Wenn das Kombinations Feld den CBS \_ -Sortier Stil hat und mithilfe von CB \_ AddString Zeichen folgen hinzugefügt werden, wirkt sich das Gebiets Schema eines Kombinations Felds darauf aus, wie Listenelemente sortiert werden.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Windows-Steuerelemente für CB_SETLOCALE Meldung
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477649"
---
# <a name="cb_setlocale-message"></a>CB- \_ setlocale-Meldung

Eine Anwendung sendet eine **CB- \_ setlocale** -Nachricht, um das aktuelle Gebiets Schema des Kombinations Felds festzulegen. Wenn das Kombinations Feld den [**CBS- \_ Sortier**](combo-box-styles.md) Stil hat und mithilfe von [**CB \_ AddString Zeichen**](cb-addstring.md)folgen hinzugefügt werden, wirkt sich das Gebiets Schema eines Kombinations Felds darauf aus, wie Listenelemente sortiert werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Gebiets Schema Bezeichner für das Kombinations Feld an, das beim Hinzufügen von Text zum Sortieren verwendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Gebiets Schema Bezeichner. Wenn *wParam* ein Gebiets Schema angibt, das nicht auf dem System installiert ist, ist der Rückgabewert CB \_ Err, und das aktuelle Kombinations Feld-Gebiets Schema wird nicht geändert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) -Makro, um einen Gebiets Schema Bezeichner und das [**makelangid-**](/windows/desktop/api/winnt/nf-winnt-makelangid) Makro zum Erstellen eines sprach Bezeichners zu erstellen. Die Sprach-ID besteht aus einer primär Sprachen-ID und einer unter Sprachen-ID.

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

[**CB \_ AddString**](cb-addstring.md)
</dt> <dt>

[**CB \_ getLocale**](cb-getlocale.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makelangid**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

