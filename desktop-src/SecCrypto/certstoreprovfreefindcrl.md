---
description: Wird aufgerufen, wenn das vom CertStoreProvFindCRL-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von CertStoreProvFindCRL nicht verwendet und daher freigegeben wurde.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Rückruffunktion "CertStoreProvFreeFindCRL"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769935"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Rückruffunktion "CertStoreProvFreeFindCRL"

Die **Rückruffunktion CertStoreProvFreeFindCRL** wird aufgerufen, wenn das vom [**CertStoreProvFindCRL-Rückruf**](certstoreprovfindcrl.md) zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **CertStoreProvFindCRL** freigegeben wurde. Bevor der CLOSE-Rückruf aufgerufen wird, müssen alle vom [**CertStoreProvFindCRL-Rückruf**](certstoreprovfindcrl.md) zurückgegebenen Zertifikate vom Anbieter mithilfe von **CertStoreProvFindCRL** oder **CertStoreProvFreeFindCRL** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hStoreProv* \[ In\]
</dt> <dd>

**HCERTSTOREPROV-Handle** für einen [*Zertifikatspeicher.*](../secgloss/c-gly.md)

</dd> <dt>

*pCrlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf einen [**\_ CRL-KONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*pvStoreProvFindInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Suchinformationen enthält.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Funktion erfolgreich ist, oder **FALSE,** wenn sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**\_CRL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
