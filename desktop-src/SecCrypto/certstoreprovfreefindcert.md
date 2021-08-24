---
description: Wird aufgerufen, wenn das vom CertStoreProvFindCert-Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von CertStoreProvFindCert freigegeben wurde.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: CertStoreProvFreeFindCert-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ab2a6ae1bd8199e7bed97626c83241223fc3943b94fcb387868331329d8740a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877300"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>CertStoreProvFreeFindCert-Rückruffunktion

Die **Rückruffunktion CertStoreProvFreeFindCert** wird aufgerufen, wenn das vom [**CertStoreProvFindCert-Rückruf**](certstoreprovfindcert.md) zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **CertStoreProvFindCert** freigegeben wurde. Bevor der CLOSE-Rückruf aufgerufen wird, müssen alle vom [**CertStoreProvFindCert-Rückruf**](certstoreprovfindcert.md) zurückgegebenen Zertifikate vom Anbieter mithilfe von **CertStoreProvFindCert** oder **CertStoreProvFreeFindCert** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ In\]
</dt> <dd>

Ein Zeiger auf einen [**CERT \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*pvStoreProvFindInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Findinformationen enthält.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Funktion erfolgreich ist, oder **FALSE,** wenn sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CERT-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
