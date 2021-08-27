---
title: TVM_HITTEST Meldung (Commctrl.h)
description: Bestimmt die Position des angegebenen Punkts relativ zum Clientbereich eines Strukturansichtssteuerelements. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-HitTest-Makros senden.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564b6d82c04c0d007784aac39284db13b3776267d524d2f615353ede50eb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060150"
---
# <a name="tvm_hittest-message"></a>TVM \_ HITTEST-Nachricht

Bestimmt die Position des angegebenen Punkts relativ zum Clientbereich eines Strukturansichtssteuerelements. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-HitTest-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVHITTESTINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) Wenn die Nachricht gesendet wird, gibt das **pt-Element** die Koordinaten des zu testden Punkts an. Wenn die Nachricht zurückgegeben wird, ist das **hItem-Element** das Handle für das Element am angegebenen Punkt oder **NULL,** wenn kein Element den Punkt einnimmt. Wenn die Nachricht zurückgegeben wird, ist der **Flags-Member** außerdem ein Treffertestwert, der die Position des angegebenen Punkts angibt. Eine Liste der Treffertestwerte finden Sie in der Beschreibung der **TVHITTESTINFO-Struktur.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Strukturansichtselement zurück, das den angegebenen Punkt einnimmt, oder **NULL,** wenn kein Element den Punkt einnimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





