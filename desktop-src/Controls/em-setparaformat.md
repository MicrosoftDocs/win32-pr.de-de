---
title: EM_SETPARAFORMAT Meldung (RichEdit. h)
description: Legt die Absatz Formatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Windows-Steuerelemente für EM_SETPARAFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476338"
---
# <a name="em_setparaformat-message"></a>EM \_ SetParaFormat-Meldung

Legt die Absatz Formatierung für die aktuelle Auswahl in einem Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur, die die neuen Absatz Formatierungs Attribute angibt. Nur die Attribute, die vom **dwMask** -Member angegeben werden, werden geändert.

Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur sein, die eine Erweiterung der [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -Struktur ist. Vor dem Senden der **EM- \_ SetParaFormat** -Meldung legen Sie den **CBSIZE** -Member der Struktur fest, um die Version der Struktur anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

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

 

 





