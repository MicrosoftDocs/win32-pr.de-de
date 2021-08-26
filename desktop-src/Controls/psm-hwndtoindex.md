---
title: PSM_HWNDTOINDEX-Nachricht (Prsht.h)
description: Übernimmt das Fensterhandle der Eigenschaftenblattseite und gibt den nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das PropSheet \_ HwndToIndex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed61c958fb3a0b30ba7cf55d1040cac51caa67f460d329312fb0e798b016aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985830"
---
# <a name="psm_hwndtoindex-message"></a>PSM \_ HWNDTOINDEX-Nachricht

Übernimmt das Fensterhandle der Eigenschaftenblattseite und gibt den nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ HwndToIndex-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Fenster der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den nullbasierten Index der Eigenschaftenblattseite zurück, die von *wParam* angegeben wird, falls erfolgreich. Andernfalls wird –1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





