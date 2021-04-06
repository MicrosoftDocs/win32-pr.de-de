---
title: MCM_GETCALENDARGRIDINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einem Kalender Raster ab.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Windows-Steuerelemente für MCM_GETCALENDARGRIDINFO Meldung
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743993"
---
# <a name="mcm_getcalendargridinfo-message"></a>MCM \_ getcalendargridinfo-Meldung

Ruft Informationen zu einem Kalender Raster ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**mcgridinfo**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) -Struktur, die Informationen über das Kalender Raster enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn erfolgreich, andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





