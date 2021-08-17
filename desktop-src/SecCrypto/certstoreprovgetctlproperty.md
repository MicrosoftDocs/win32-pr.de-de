---
description: Ruft eine angegebene Eigenschaft einer Zertifikatvertrauensliste (Certificate Trust List, CTL) ab.
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Rückruffunktion "CertStoreProvGetCTLProperty"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769759"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Rückruffunktion "CertStoreProvGetCTLProperty"

Die **Rückruffunktion CertStoreProvGetCTLProperty** ruft eine angegebene Eigenschaft einer [*Zertifikatvertrauensliste (Certificate Trust List,*](../secgloss/c-gly.md) CTL) ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

Ein **HCERTSTOREPROV-Handle** für einen [*Zertifikatspeicher.*](../secgloss/c-gly.md)

</dd> <dt>

*pCtlContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CTL \_ CONTEXT-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

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

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CTL \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) enthält, die von der Funktion zurückgegeben werden soll. Um den Wert von *"pwData"* abzurufen, bevor Speicher für den Puffer zugewiesen wird, kann dieser Parameter bei einem ersten Aufruf der Funktion auf **NULL** festgelegt werden.

</dd> <dt>

*data* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD,** das die Länge des *pvData-Puffers* angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion einen Wert ungleich 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CTL-KONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
