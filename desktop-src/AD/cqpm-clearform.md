---
title: CQPM_CLEARFORM Meldung (Cmnquery.h)
description: Wird an die Rückruffunktion CQPageProc einer Abfrage für eine Erweiterungsseite gesendet, wenn der Inhalt der Seite auf die Standardwerte zurückgesetzt werden soll.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- CQPM_CLEARFORM-Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f900542c631193057985ca70d81dbfa7d3e53c6602f81a69b4e61a7cd107641a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021366"
---
# <a name="cqpm_clearform-message"></a>CQPM \_ CLEARFORM-Nachricht

Die **CQPM \_ CLEARFORM-Nachricht** wird an die [**Rückruffunktion CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) einer Abfrage für eine Erweiterungsseite gesendet, wenn der Inhalt der Seite auf die Standardwerte zurückgesetzt werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **S \_ OK** zurück, wenn erfolgreich, oder andernfalls ein HRESULT-Standardfehlercode. 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





