---
title: PBM_SETMARQUEE Meldung (kommstrg. h)
description: Legt die Statusanzeige auf den Marquee-Modus fest. Dies bewirkt, dass die Statusanzeige wie ein Marquee verschoben wird.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Windows-Steuerelemente für PBM_SETMARQUEE Meldung
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956811"
---
# <a name="pbm_setmarquee-message"></a>PBM- \_ setmarquee-Nachricht

Legt die Statusanzeige auf den Marquee-Modus fest. Dies bewirkt, dass die Statusanzeige wie ein Marquee verschoben wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Marquee-Modus aktiviert oder deaktiviert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Zeit (in Millisekunden) zwischen der Aktualisierung der Marquee-Animation. Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung, wenn Sie den Fortschritt im Hinblick auf den Abschluss nicht kennen, aber angeben möchten, dass der Fortschritt ausgeführt wird.

Senden Sie die **PBM- \_ setmarquee** -Nachricht, um die Animation zu starten oder zu unterbinden.

> [!Note]  
> Sie müssen den Steuer Stil des Steuer Elements auf [**PSB- \_ Marquee**](progress-bar-control-styles.md) festlegen, bevor Sie versuchen, die Animation zu starten.

 

> [!Note]  
> Diese Meldung erfordert ComCtl32.dll-Version 6,00 oder höher.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





