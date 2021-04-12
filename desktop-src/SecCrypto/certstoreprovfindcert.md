---
description: Listet das erste oder nächste Zertifikat in einem externen Speicher auf, das den angegebenen Kriterien entspricht, oder ermittelt es.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Certstoreprovfindcert-Rückruffunktion
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
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347078"
---
# <a name="certstoreprovfindcert-callback-function"></a>Certstoreprovfindcert-Rückruffunktion

Die **certstoreprovfindcert** -Rückruffunktion listet das erste oder nächste Zertifikat in einem [*externen Speicher*](../secgloss/e-gly.md) auf, das den angegebenen Kriterien entspricht.

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

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pfindinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an die [**certfindcertifikateinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) -Funktion übergeben werden.

</dd> <dt>

*pprevcertcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des gefundenen Zertifikats. Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden. Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovcertcontext* -Parameter zurückgegeben wurde. Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> <dt>

*ppvstoreprovfindinfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben. Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben. Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.

</dd> <dt>

*ppprovcertcontext* \[ vorgenommen\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf das gefundene Zertifikat zurückgegeben.

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

[**CERT \_ Store \_ Prov \_ Find \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**Certfindcertifi. Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
