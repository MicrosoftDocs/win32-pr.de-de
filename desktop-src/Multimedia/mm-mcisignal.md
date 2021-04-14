---
title: MM_MCISIGNAL Meldung (MMSYSTEM. h)
description: Die mm \_ mcisignal-Nachricht wird an ein Fenster gesendet, um eine Anwendung zu benachrichtigen, dass ein MCI-Gerät eine in einem vorherigen Signal (MCI-Signal)-Befehl definierte Position erreicht hat \_ .
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392093"
---
# <a name="mm_mcisignal-message"></a>MM- \_ mcisignal-Meldung

Die **mm \_ mcisignal** -Nachricht wird an ein Fenster gesendet, um eine Anwendung zu benachrichtigen, dass ein MCI-Gerät eine in einem vorherigen [**Signal**](signal.md) ( [**MCI- \_ Signal**](mci-signal.md))-Befehl definierte Position erreicht hat.


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Der Bezeichner des Geräts, von dem die Signal Meldung initiiert wird.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*luserparamem*
</dt> <dd>

Der Wert, der im **dwuserparamem** -Member der **MCI \_ DGV-Signal \_ parametriams \_** -Struktur übermittelt wird, wenn der **Signal** -Befehl diese Rückruffunktion definiert hat. Alternativ kann Sie auch den Positionswert enthalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Nachrichten](mci-messages.md)
</dt> <dt>

[**aussendet**](signal.md)
</dt> </dl>

 

 





