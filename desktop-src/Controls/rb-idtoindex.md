---
title: RB_IDTOINDEX Nachricht (Commctrl.h)
description: Konvertiert einen Bandbezeichner in einen Bandindex in einem Rebar-Steuerelement.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b13d243498d821e64be19beebb04fab3f198442aced73ced6f424d32d7177ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642600"
---
# <a name="rb_idtoindex-message"></a>\_RB-IDTOINDEX-Nachricht

Konvertiert einen Bandbezeichner in einen Bandindex in einem Rebar-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der anwendungsdefinierte Bezeichner des betreffenden Bands. Dies ist der Wert, der im **wID-Member** der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) übergeben wurde, als das Band eingefügt wurde.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den nullbasierten Bandindex zurück, andernfalls -1. Wenn doppelte Bandbezeichner vorhanden sind, wird der erste zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





