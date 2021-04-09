---
title: EM_GETSELTEXT Meldung (RichEdit. h)
description: Ruft den aktuell ausgewählten Text in einem Rich-Edit-Steuerelement ab.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Windows-Steuerelemente für EM_GETSELTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858851"
---
# <a name="em_getseltext-message"></a>EM \_ GetSelText-Nachricht

Ruft den aktuell ausgewählten Text in einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den ausgewählten Text empfängt. Die aufrufenden Anwendung muss sicherstellen, dass der Puffer groß genug ist, um den ausgewählten Text zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der kopierten Zeichen ohne das abschließende Null Zeichen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





