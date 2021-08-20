---
description: Aufzählt oder sucht die erste oder nächste Zertifikatsperrliste in einem externen Speicher, der den angegebenen Kriterien entspricht.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: CertStoreProvFindCRL-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: eebcc990da0cd2d866325200223e9e654e45e055299a8b384a613dc9841c2799
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126680"
---
# <a name="certstoreprovfindcrl-callback-function"></a>CertStoreProvFindCRL-Rückruffunktion

Die **Rückruffunktion CertStoreProvFindCRL** listet die erste oder nächste [*Zertifikatsperrliste*](../secgloss/c-gly.md) in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder sucht sie. [](../secgloss/e-gly.md)

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Ein Zeiger auf eine [**CERT \_ STORE \_ PROV \_ FIND \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) mit allen Parametern, die an die [**CertFindCRLInStore-Funktion übergeben**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) werden.

</dd> <dt>

*pPrevCrlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) der letzten gefundenen Zertifikatsperrliste. Beim ersten Aufruf der Funktion sollte dieser Parameter auf NULL **festgelegt werden.** Bei nachfolgenden Aufrufen sollte sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppProvCRLContext-Parameter* zurückgegeben wurde. Ein in diesem Parameter übergebener **Nicht-NULL-Zeiger** wird von der Rückruffunktion frei.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen Puffer, um die Speicheranbieterinformationen zurück zu geben. Optional kann der Rückruf einen Zeiger auf interne Find-Informationen in diesem Parameter zurückgeben. Nach dem ersten Aufruf wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufruf der Funktion zurückgegeben wurde.

</dd> <dt>

*ppProvCrlContext* \[ out\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene Zertifikatsperrliste zurückgegeben.

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

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**\_CRL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
