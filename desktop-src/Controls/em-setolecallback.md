---
title: EM_SETOLECALLBACK Meldung (RichEdit. h)
description: Ermöglicht einem Rich-Edit-Steuerelement ein IRichEditOleCallback-Objekt, das das Steuerelement verwendet, um OLE-bezogene Ressourcen und Informationen vom Client abzurufen.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- Windows-Steuerelemente für EM_SETOLECALLBACK Meldung
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956637"
---
# <a name="em_setolecallback-message"></a>EM- \_ Nachricht

Ermöglicht einem Rich-Edit-Steuerelement ein [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Objekt, das das Steuerelement verwendet, um OLE-bezogene Ressourcen und Informationen vom Client abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) -Objekt. Das-Steuerelement ruft vor der Rückgabe die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode für das-Objekt auf.

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



 

