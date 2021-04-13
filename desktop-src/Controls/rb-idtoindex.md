---
title: RB_IDTOINDEX Meldung (kommstrg. h)
description: Konvertiert einen Band Bezeichner in einen Band-Index in einem Grund leisten-Steuerelement.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- Windows-Steuerelemente für RB_IDTOINDEX Meldung
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
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475345"
---
# <a name="rb_idtoindex-message"></a>RB \_ iddeindex-Meldung

Konvertiert einen Band Bezeichner in einen Band-Index in einem Grund leisten-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der von der Anwendung definierte Bezeichner des fraglichen Bands. Dies ist der Wert, der beim Einfügen des Bands im **wID** -Member der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur weitergegeben wurde.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NULL basierten BandIndex zurück, wenn erfolgreich, andernfalls-1. Wenn doppelte Band Bezeichner vorhanden sind, wird der erste zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





