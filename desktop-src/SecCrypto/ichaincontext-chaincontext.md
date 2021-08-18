---
description: Legt den PCCERT CHAIN CONTEXT eines Zertifikats fest oder ruft sie \_ \_ ab.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: IChainContext::ChainContext-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005498"
---
# <a name="ichaincontextchaincontext-property"></a>IChainContext::ChainContext-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **ChainContext-Eigenschaft** legt den PCCERT CHAIN CONTEXT eines Zertifikats fest oder ruft sie \_ \_ ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der PCCERT \_ CHAIN \_ CONTEXT des Zertifikats.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaftenzugriffsmethoden **\_ ChainContext setzen** und **\_ ChainContext** erfolgreich abrufen, geben sie S \_ OK zurück.

Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Sie müssen entweder die [**FreeContext-Methode**](ichaincontext-freecontext.md) oder die [**CertFreeCertificateChain-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) aufrufen, um den Kontext freizugeben.

Wenn Sie die **ChainContext-Eigenschaft** festlegen, wird der Zustand des gesamten [**Chain-Objekts**](chain.md) zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




