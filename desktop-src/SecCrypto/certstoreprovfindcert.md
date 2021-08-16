---
description: Aufzählt oder sucht das erste oder nächste Zertifikat in einem externen Speicher, der den angegebenen Kriterien entspricht.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: CertStoreProvFindCert-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770019"
---
# <a name="certstoreprovfindcert-callback-function"></a>CertStoreProvFindCert-Rückruffunktion

Die **Rückruffunktion CertStoreProvFindCert** listet das erste oder nächste Zertifikat [](../secgloss/e-gly.md) in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder findet es.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hStoreProv* \[ In\]
</dt> <dd>

**HCERTSTOREPROV-Handle** für einen [*Zertifikatspeicher.*](../secgloss/c-gly.md)

</dd> <dt>

*pFindInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CERT \_ STORE \_ PROV \_ FIND \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) mit allen Parametern, die an die [**CertFindCertificateInStore-Funktion übergeben**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) werden.

</dd> <dt>

*pPrevCertContext* \[ In\]
</dt> <dd>

Ein Zeiger auf einen [**CERT \_ CONTEXT des**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) gefundenen Zertifikats. Beim ersten Aufruf der Funktion sollte dieser Parameter auf NULL **festgelegt werden.** Bei nachfolgenden Aufrufen sollte sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppProvCertContext-Parameter* zurückgegeben wurde. Ein in diesem Parameter übergebener **Nicht-NULL-Zeiger** wird von der Rückruffunktion frei.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen Puffer, um die Speicheranbieterinformationen zurück zu geben. Optional kann der Rückruf einen Zeiger auf interne Find-Informationen in diesem Parameter zurückgeben. Nach dem ersten Aufruf wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufruf der Funktion zurückgegeben wurde.

</dd> <dt>

*ppProvCertContext* \[ out\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf das gefundene Zertifikat zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Funktion erfolgreich ist, oder **FALSE,** wenn sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CERT-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
