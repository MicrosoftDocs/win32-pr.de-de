---
title: CQPM_ENABLE Nachricht (Cmnquery.h)
description: Wird an die Rückruffunktion CQPageProc einer Abfrageformularerweiterungsseite gesendet, um die Seite zu aktivieren oder zu deaktivieren.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- CQPM_ENABLE-Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653ecd692d5cba425112afb2a110cb905fd26c31175fafc1ec7501dea619b709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021356"
---
# <a name="cqpm_enable-message"></a>CQPM \_ ENABLE-Nachricht

Die **CQPM \_ ENABLE-Nachricht** wird an die [**Rückruffunktion CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) einer Abfrageformularerweiterungsseite gesendet, um die Seite zu aktivieren oder zu deaktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält 0 (null), um die Seite zu deaktivieren, oder ungleich 0 (null), um die Seite zu aktivieren.

</dd> <dt>

*lParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird ignoriert.

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

 

 





