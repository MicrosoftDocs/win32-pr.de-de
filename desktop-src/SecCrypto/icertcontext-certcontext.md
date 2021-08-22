---
description: Legt den PCCERT CONTEXT eines Zertifikats \_ fest oder ruft sie ab.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: ICertContext::CertContext-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5c517384bdffd8723c1e9e0d96683cc4bd4918361acdf19df77286bfbac962b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006368"
---
# <a name="icertcontextcertcontext-property"></a>ICertContext::CertContext-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **CertContext-Eigenschaft** legt den PCCERT CONTEXT eines Zertifikats fest \_ oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der PCCERT \_ CONTEXT des Zertifikats.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaftenzugriffsmethoden **\_ CertContext verwenden** und **\_ CertContext** erfolgreich erhalten, geben sie S \_ OK zurück.

Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Sie müssen entweder die [**FreeContext-Methode**](icertcontext-freecontext.md) oder die [**CertFreeCertificateContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) aufrufen, um den Kontext frei zu geben.

Wenn Sie die **CertContext-Eigenschaft** festlegen, wird der Status des gesamten [**Certificate-Objekts**](certificate.md) zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




