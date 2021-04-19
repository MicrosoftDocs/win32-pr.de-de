---
description: Wird aufgerufen, wenn das vom certstoreprovfindcert-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindcert nicht verwendet und daher freigegeben wurde.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Certstoreprovfrefindcert-Rückruffunktion
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
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353846"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Certstoreprovfrefindcert-Rückruffunktion

Die **certstoreprovfrefindcert** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindcert**](certstoreprovfindcert.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **certstoreprovfindcert** freigegeben wurde. Bevor der Close-Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindcert**](certstoreprovfindcert.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindcert** oder **certstoreprovfreifindcert** freigegeben werden.

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

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pcertcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

</dd> <dt>

*pvstoreprovfindinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Informationen zu suchen enthält.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**Certstoreprovfindcert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
