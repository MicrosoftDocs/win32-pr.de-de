---
description: Listet die erste oder nächste Zertifikat Sperr Liste in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder ermittelt Sie.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Certstoreprovfindcrl-Rückruffunktion
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
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529711"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Certstoreprovfindcrl-Rückruffunktion

Die **certstoreprovfindcrl** -Rückruffunktion listet die erste oder die nächste [*CRL*](../secgloss/c-gly.md) in einem externen [*Speicher*](../secgloss/e-gly.md) auf, die den angegebenen Kriterien entspricht, oder sucht Sie.

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

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pfindinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an die [**certfindcrlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) -Funktion übergeben werden.

</dd> <dt>

*pprevcrlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur der letzten gefundenen CRL. Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden. Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovcrlcontext* -Parameter zurückgegeben wurde. Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> <dt>

*ppvstoreprovfindinfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben. Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben. Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.

</dd> <dt>

*ppprovcrlcontext* \[ vorgenommen\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene CRL zurückgegeben.

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

[**CERT \_ Store \_ Prov \_ Find \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**Certfindcrlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
