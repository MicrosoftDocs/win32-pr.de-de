---
description: Wird aufgerufen, wenn das vom CertStoreProvFindCTL-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von CertStoreProvFindCTL nicht verwendet und daher freigegeben wurde.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: CertStoreProvFreeFindCTL-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5f3f6d224ed19073408015b3b83b90a66e9402d9b838d50eb7a8381e312e0534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877140"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>CertStoreProvFreeFindCTL-Rückruffunktion

Die **Rückruffunktion CertStoreProvFreeFindCTL** wird aufgerufen, wenn das vom [**CertStoreProvFindCTL-Rückruf**](certstoreprovfindctl.md) zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **CertStoreProvFindCTL** freigegeben wurde. Bevor der CLOSE-Rückruf aufgerufen wird, müssen alle vom [**CertStoreProvFindCTL-Rückruf**](certstoreprovfindctl.md) zurückgegebenen Zertifikate vom Anbieter mithilfe von **CertStoreProvFindCTL** oder **CertStoreProvFreeFindCTL** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

*pCtlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CTL \_ CONTEXT-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**\_CTL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
