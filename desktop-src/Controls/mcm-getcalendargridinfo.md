---
title: MCM_GETCALENDARGRIDINFO (Commctrl.h)
description: Ruft Informationen zu einem Kalenderraster ab.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO meldungssteuerelemente Windows
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
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170167"
---
# <a name="mcm_getcalendargridinfo-message"></a>MCM \_ GETCALENDARGRIDINFO-Meldung

Ruft Informationen zu einem Kalenderraster ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**MCGRIDINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) die Informationen zum Kalenderraster enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn erfolgreich, **andernfalls FALSE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





