---
title: EM_PASTESPECIAL Meldung (RichEdit. h)
description: Fügt ein bestimmtes Zwischenablage Format in einem Rich-Edit-Steuerelement ein.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Windows-Steuerelemente für EM_PASTESPECIAL Meldung
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859016"
---
# <a name="em_pastespecial-message"></a>\_Gepastespecial Nachricht

Fügt ein bestimmtes Zwischenablage Format in einem Rich-Edit-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die [Zwischenablage Formate](/windows/desktop/dataxchg/clipboard-formats)an.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**repastespecial**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) -Struktur oder **null**. Wenn ein Objekt eingefügt wird, wird die **repastespecial** -Struktur mit dem gewünschten Anzeige Aspekt ausgefüllt. Wenn *LPARAM* **null** ist oder der **dwAspect** -Member 0 (null) ist, ist der verwendete Anzeige Aspekt der Inhalt des Objekt Deskriptors.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Repastespecial**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

