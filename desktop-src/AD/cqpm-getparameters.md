---
title: CQPM_GETPARAMETERS Meldung (Cmnquery.h)
description: Wird an die CQPageProc-Rückruffunktion einer Abfrageformularerweiterungsseite gesendet, um Daten über die von der Seite ausgeführte Abfrage abzurufen.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS-Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64713c79fc2c1b72f1962363f1330ecd794ad804f0ab084b66c134c66133cd82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021231"
---
# <a name="cqpm_getparameters-message"></a>CQPM \_ GETPARAMETERS-Nachricht

Die **CQPM \_ GETPARAMETERS-Nachricht** wird an die [**CQPageProc-Rückruffunktion**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) einer Abfrageformularerweiterungsseite gesendet, um Daten über die von der Seite ausgeführte Abfrage abzurufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen [**LPDSQUERYPARAMS-Wert,**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) der Daten über die von der Seite ausgeführte Abfrage empfängt. Wenn dieser Parameter **NULL** ist, muss die **DSQUERYPARAMS-Struktur** von der Erweiterung mithilfe der [**CoTaskMemAlloc-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) zugeordnet werden.

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
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

