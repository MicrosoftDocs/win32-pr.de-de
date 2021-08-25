---
description: Ruft eine angegebene Eigenschaft einer Sperrliste ab.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Rückruffunktion "CertStoreProvGetCRLProperty"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877050"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Rückruffunktion "CertStoreProvGetCRLProperty"

Die **Rückruffunktion CertStoreProvGetCRLProperty** ruft eine angegebene Eigenschaft einer [*Zertifikatsperrliste*](../secgloss/c-gly.md)ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRL \_ CONTEXT-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)

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

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CRL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) enthält, die von der Funktion zurückgegeben werden soll. Kann bei einem ersten Aufruf der Funktion auf **NULL** festgelegt werden, um den Wert von *"data"* abzurufen, bevor Arbeitsspeicher für den Puffer zugewiesen wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CRL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
