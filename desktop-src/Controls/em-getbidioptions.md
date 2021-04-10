---
title: EM_GETBIDIOPTIONS Meldung (RichEdit. h)
description: Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement an.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Windows-Steuerelemente für EM_GETBIDIOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104048"
---
# <a name="em_getbidioptions-message"></a>EM \_ getbidioptions-Meldung

Gibt den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) -Struktur, die den aktuellen Zustand der bidirektionalen Optionen im Rich Edit-Steuerelement empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung legt die Werte der **wmask** -und **weffects** -Elemente auf den Wert des aktuellen Status der bidirektionalen Optionen im Rich Edit-Steuerelement fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ setbidioptions**](em-setbidioptions.md)
</dt> </dl>

 

 





