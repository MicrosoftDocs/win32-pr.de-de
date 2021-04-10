---
title: EM_SETCTFOPENSTATUS Meldung (RichEdit. h)
description: Öffnet oder schließt die TSF-Tastatur (Text Services Framework).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Windows-Steuerelemente für EM_SETCTFOPENSTATUS Meldung
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040899"
---
# <a name="em_setctfopenstatus-message"></a>EM \_ setctfopenstatus-Meldung

Öffnet oder schließt die TSF-Tastatur (Text Services Framework).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Verwenden Sie " **true**", um die TSF-Tastatur zu aktivieren. Um die TSF-Tastatur zu deaktivieren, verwenden Sie **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Meldung **true** zurück. Wenn nicht erfolgreich, gibt diese Meldung **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getctfopenstatus**](em-getctfopenstatus.md)
</dt> </dl>

 

 





