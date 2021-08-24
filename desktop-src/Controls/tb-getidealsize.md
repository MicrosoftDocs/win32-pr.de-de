---
title: TB_GETIDEALSIZE Meldung (Commctrl.h)
description: Ruft die ideale Größe der Symbolleiste ab.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1844f3ae4200c1120f784c03e5f80d2df4457319cf81e12c88ce0ed84525117d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816310"
---
# <a name="tb_getidealsize-message"></a>TB \_ GETIDEALSIZE-Nachricht

Ruft die ideale Größe der Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Eine **BOOL,** die angibt, ob die ideale Höhe oder Breite der Symbolleiste abgerufen werden soll. Verwenden Sie **TRUE,** um die ideale Höhe abzurufen, **FALSE,** um die ideale Breite abzurufen.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SIZE-Struktur,**](/previous-versions//dd145106(v=vs.85)) die die Höhe oder Breite empfängt, an der alle Schaltflächen angezeigt werden. Wenn *wParam* **TRUE** ist, ist nur das **Cy-Element** (Höhe) gültig. Wenn *wParam* **FALSE** ist, ist nur der **cx-Member** (Breite) gültig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

