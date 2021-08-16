---
description: Ruft eine angegebene Eigenschaft eines Zertifikats ab.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Rückruffunktion "CertStoreProvGetCertProperty"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769925"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Rückruffunktion "CertStoreProvGetCertProperty"

Die **Rückruffunktion CertStoreProvGetCertProperty** ruft eine angegebene Eigenschaft eines Zertifikats ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
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

Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*dwPropId* \[ In\]
</dt> <dd>

Gibt einen Eigenschaftenbezeichner an.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Alle erforderlichen Flagwerte.

</dd> <dt>

*pvData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CERT \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) enthält, die von der Funktion zurückgegeben werden soll. Kann bei einem ersten Aufruf der Funktion auf **NULL** festgelegt werden, um den Wert von *"data"* abzurufen, bevor Arbeitsspeicher für den Puffer zugewiesen wird.

</dd> <dt>

*data* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD,** der die Länge des *pvData-Puffers* angibt.

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

[**\_CERT-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
