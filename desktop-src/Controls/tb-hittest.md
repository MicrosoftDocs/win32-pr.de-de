---
title: TB_HITTEST Meldung (kommstrg. h)
description: Bestimmt, wo sich ein Punkt in einem ToolBar-Steuerelement befindet.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Windows-Steuerelemente für TB_HITTEST Meldung
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949697"
---
# <a name="tb_hittest-message"></a>TB- \_ HitTest-Meldung

Bestimmt, wo sich ein Punkt in einem ToolBar-Steuerelement befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die x-Koordinate des Treffer Tests im **x** -Element und die y-Koordinate des Treffer Tests im **y** -Member enthält. Die Koordinaten sind relativ zum Client Bereich der Symbolleiste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück. Wenn der Rückgabewert 0 (null) oder ein positiver Wert ist, handelt es sich um den NULL basierten Index des nicht Trennzeichens, in dem sich der Punkt befindet. Wenn der Rückgabewert negativ ist, liegt der Punkt nicht innerhalb einer Schaltfläche. Der absolute Wert des Rückgabewerts ist der Index eines Trenn Zeichens oder das nächste nicht Trennzeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

