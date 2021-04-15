---
title: CQPM_SETDEFAULTPARAMETERS Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um alternative Standardparameter für die Seite festzulegen.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476491"
---
# <a name="cqpm_setdefaultparameters-message"></a>Cqpm- \_ setdefaultparameters-Meldung

Die **cqpm- \_ setdefaultparameters** -Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, um alternative Standardparameter für die Seite festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält einen Wert ungleich 0 (null), wenn die Seite die Standardseite ist, andernfalls NULL.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**openquerywindow**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) -Struktur, die Daten zum Dialogfeld Verzeichnisdienst Abfrage enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**Openquerywindow**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





