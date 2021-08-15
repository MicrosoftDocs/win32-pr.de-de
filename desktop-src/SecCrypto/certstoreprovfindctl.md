---
description: Listet die erste oder nächste CTL in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder sucht sie.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: CertStoreProvFindCTL-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f3064b42961196a7522fba6d08ac684aa4421b26727cdf229854351c777a4b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770007"
---
# <a name="certstoreprovfindctl-callback-function"></a>CertStoreProvFindCTL-Rückruffunktion

Die **Rückruffunktion CertStoreProvFindCTL** listet die erste oder nächste [*CTL*](../secgloss/c-gly.md) in einem [*externen Speicher*](../secgloss/e-gly.md) auf, der den angegebenen Kriterien entspricht, oder sucht diese.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
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

Ein Zeiger auf eine [**CERT \_ STORE \_ PROV \_ FIND \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) die alle Parameter enthält, die an [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)übergeben werden. Funktion zurückgegeben wird.

</dd> <dt>

*pPrevCtlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CTL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) der letzten gefundenen CTL. Beim ersten Aufruf der Funktion sollte dieser Parameter auf **NULL** festgelegt werden. Bei nachfolgenden Aufrufen sollte er auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppProvCTLContext-Parameter* zurückgegeben wird. Ein in diesem Parameter übergebener Zeiger ungleich **NULL** wird von der Rückruffunktion freigegeben.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf den Puffer, um die Speicheranbieterinformationen zurückzugeben. Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben. Nach dem ersten Aufruf wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufruf der Funktion zurückgegeben wurde.

</dd> <dt>

*ppProvCtlContext* \[ out\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene CTL zurückgegeben.

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

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**\_CTL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
