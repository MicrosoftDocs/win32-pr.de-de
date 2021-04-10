---
title: TVM_HITTEST Meldung (kommstrg. h)
description: Bestimmt den Speicherort des angegebenen Punkts relativ zum Client Bereich eines Strukturansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ HitTest-Makros senden.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Windows-Steuerelemente für TVM_HITTEST Meldung
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
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040348"
---
# <a name="tvm_hittest-message"></a>TVM- \_ HitTest-Meldung

Bestimmt den Speicherort des angegebenen Punkts relativ zum Client Bereich eines Strukturansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) -Struktur. Wenn die Nachricht gesendet wird, gibt der **PT** -Member die Koordinaten des zu testenden Punkts an. Wenn die Meldung zurückgegeben wird, ist das **Hitem** -Element das Handle für das Element am angegebenen Punkt oder **null** , wenn kein Element den Punkt einnimmt. Wenn die Nachricht zurückgegeben wird, ist der **Flags** -Member außerdem ein Treffer Testwert, der die Position des angegebenen Punkts angibt. Eine Liste der Treffer Test Werte finden Sie in der Beschreibung der **TVHITTESTINFO** -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Struktur Ansichts Element zurück, das den angegebenen Punkt einnimmt, oder **null** , wenn kein Element den Punkt einnimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





