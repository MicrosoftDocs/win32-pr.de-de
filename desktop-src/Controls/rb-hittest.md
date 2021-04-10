---
title: RB_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welcher Teil eines Grund leisten Bands an einem bestimmten Punkt auf dem Bildschirm angezeigt wird, wenn ein Info leisten-Band an diesem Punkt vorhanden ist.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Windows-Steuerelemente für RB_HITTEST Meldung
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040165"
---
# <a name="rb_hittest-message"></a>RB \_ HitTest-Meldung

Bestimmt, welcher Teil eines Grund leisten Bands an einem bestimmten Punkt auf dem Bildschirm angezeigt wird, wenn ein Info leisten-Band an diesem Punkt vorhanden ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**rbhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) -Struktur. Bevor die Nachricht gesendet wird, muss der **PT** -Member dieser Struktur in Client Koordinaten mit dem Punkt initialisiert werden, der als Treffer getestet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NULL basierten Index des Bands am angegebenen Punkt zurück, oder-1, wenn sich kein Grund leisten Band am Punkt befand.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





