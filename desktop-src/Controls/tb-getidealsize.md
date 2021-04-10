---
title: TB_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die ideale Größe der Symbolleiste ab.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Windows-Steuerelemente für TB_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040234"
---
# <a name="tb_getidealsize-message"></a>TB- \_ getidealsize-Nachricht

Ruft die ideale Größe der Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Ein **boolescher** Wert, der angibt, ob die ideale Höhe oder Breite der Symbolleiste abgerufen wird. Verwenden Sie " **true** ", um die ideale Höhe abzurufen, " **false** ", um die ideale Breite abzurufen.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die Höhe oder Breite empfängt, bei der alle Schaltflächen angezeigt werden. Wenn *wParam* den Wert **true** hat, ist nur der **CY** -Member (Height) gültig. Wenn *wParam* den Wert **false** hat, ist nur der **CX** -Member (Width) gültig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

