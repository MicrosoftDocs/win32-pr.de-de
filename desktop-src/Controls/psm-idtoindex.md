---
title: PSM_IDTOINDEX (Prsht.h)
description: Verwendet die Ressourcen-ID einer Eigenschaftenblattseite und gibt ihren nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das PropSheet \_ IdToIndex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX-Windows Steuerelemente
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83bce0bfeecd2f233b2108133b08e49c27c90625c1bd07f2d4273bd77bbd0b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061520"
---
# <a name="psm_idtoindex-message"></a>PSM \_ IDTOINDEX-Nachricht

Verwendet die Ressourcen-ID einer Eigenschaftenblattseite und gibt ihren nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IdToIndex-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ressourcen-ID der Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den nullbasierten Index der Eigenschaftenblattseite zurück, die *von lParam* angegeben wird. Andernfalls wird –1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





