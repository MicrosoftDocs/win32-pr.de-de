---
description: Listet die erste oder nächste CTL in einem externen Speicher auf, der den angegebenen Kriterien entspricht, oder sucht Sie.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Certstoreprovfindctl-Rückruffunktion
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
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362385"
---
# <a name="certstoreprovfindctl-callback-function"></a>Certstoreprovfindctl-Rückruffunktion

Die **certstoreprovfindctl** -Rückruffunktion listet die erste oder nächste [*CTL*](../secgloss/c-gly.md) in einem [*externen Speicher*](../secgloss/e-gly.md) auf, der den angegebenen Kriterien entspricht.

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

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pfindinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Zertifikat \_ Speicher- \_ Prov- \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) Struktur, die alle Parameter enthält, die an den [**certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)übergeben werden. Funktion zurückgegeben wird.

</dd> <dt>

*pprevctlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur der letzten gefundenen CTL. Beim ersten Aufrufen der-Funktion sollte dieser Parameter auf **null** festgelegt werden. Bei nachfolgenden Aufrufen sollte Sie auf den Zeiger festgelegt werden, der beim letzten Aufruf im *ppprovctlcontext* -Parameter zurückgegeben wurde. Ein nicht-**null** -Zeiger, der in diesem Parameter übergeben wird, wird von der Rückruffunktion freigegeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> <dt>

*ppvstoreprovfindinfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen Puffer, um die Informationen zum Speicher Anbieter zurückzugeben. Optional kann der Rückruf einen Zeiger auf interne Suchinformationen in diesem Parameter zurückgeben. Nach dem ersten-Befehl wird dieser Parameter auf den Zeiger festgelegt, der durch den vorherigen Aufrufen der-Funktion zurückgegeben wurde.

</dd> <dt>

*ppprovctlcontext* \[ vorgenommen\]
</dt> <dd>

Bei einer erfolgreichen Suche wird in diesem Parameter ein Zeiger auf die gefundene CTL-Datei zurückgegeben.

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

[**Certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
