---
title: RB_GETBANDINFO-Nachricht (Commctrl.h)
description: Ruft Informationen zu einem angegebenen Band in einem Rebar-Steuerelement ab.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409441"
---
# <a name="rb_getbandinfo-message"></a>RB \_ GETBANDINFO-Meldung

Ruft Informationen zu einem angegebenen Band in einem Rebar-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Bands, für das die Informationen abgerufen werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**REBARBANDINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) die die angeforderten Bandinformationen empfängt. Bevor Sie diese Nachricht senden, müssen Sie den **cbSize-Member** dieser Struktur auf die Größe der **REBARBANDINFO-Struktur** und den **fMask-Member** auf die Elemente festlegen, die Sie abrufen möchten. Darüber hinaus müssen Sie den **cch-Member** der **REBARBANDINFO-Struktur** auf die Größe des **lpText-Puffers** festlegen, wenn RBBIM \_ TEXT angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ GETBANDINFOW** (Unicode) und **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





