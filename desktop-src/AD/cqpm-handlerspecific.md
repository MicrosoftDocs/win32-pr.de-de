---
title: CQPM_HANDLERSPECIFIC Meldung (cmnquery. h)
description: Basiswert, der für Nachrichten verwendet wird, die für den Abfrage Handler privat sind.
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475585"
---
# <a name="cqpm_handlerspecific-message"></a>Cqpm- \_ handlerspecific-Meldung

Die **cqpm \_ handlerspecific** -Meldung ist der Basiswert, der für Nachrichten verwendet wird, die für den Abfrage Handler privat sind. Der Abfrage Handler sollte diesen Wert privaten Nachrichten hinzufügen, um sicherzustellen, dass keine Nachrichten Konflikte auftreten.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält zusätzliche Nachrichten Daten. Der Inhalt dieses Parameters wird vom Abfrage Handler definiert.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält zusätzliche Nachrichten Daten. Der Inhalt dieses Parameters wird vom Abfrage Handler definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Bedeutung des Rückgabewerts wird durch den Abfrage Handler definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





