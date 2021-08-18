---
description: Gibt einen PCCERT \_ CONTEXT frei, der über die CertContext-Eigenschaft erworben wurde.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: ICertContext::FreeContext-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006188"
---
# <a name="icertcontextfreecontext-method"></a>ICertContext::FreeContext-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **FreeContext-Methode** gibt einen PCCERT \_ CONTEXT frei, der über die [**CertContext-Eigenschaft erworben**](icertcontext-certcontext.md) wurde.

## <a name="syntax"></a>Syntax


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCertContext* \[ In\]
</dt> <dd>

Der PCCERT \_ CONTEXT, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt den Erfolg an. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Diese Methode gibt den PCCERT CONTEXT, der in einem Certificate-Objekt enthalten \_ [**ist, nicht**](certificate.md) frei. Sie sollte nur verwendet werden, um einen PCCERT CONTEXT frei zu geben, \_ der über die [**CertContext-Eigenschaft erworben**](icertcontext-certcontext.md) wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




