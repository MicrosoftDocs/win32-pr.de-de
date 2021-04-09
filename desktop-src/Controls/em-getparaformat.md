---
title: EM_GETPARAFORMAT Meldung (RichEdit. h)
description: Ruft die Absatz Formatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Windows-Steuerelemente für EM_GETPARAFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957005"
---
# <a name="em_getparaformat-message"></a>EM \_ GetParaFormat-Meldung

Ruft die Absatz Formatierung der aktuellen Auswahl in einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur, die die Absatz Formatierungs Attribute der aktuellen Auswahl empfängt.

Wenn mehr als ein Absatz ausgewählt ist, empfängt die Struktur die Attribute des ersten Absatzes, und der **dwMask** -Member gibt an, welche Attribute in der gesamten Auswahl konsistent sind.

Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur sein, die eine Erweiterung der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur ist. Vor dem Senden der **EM \_ GetParaFormat** -Meldung legen Sie den **CBSIZE** -Member der Struktur so fest, dass die Version der Struktur angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt den Wert des **dwMask** -Members der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





