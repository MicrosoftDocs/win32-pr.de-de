---
description: Gibt einen pccert-kontextfrei, \_ der über die certcontext-Eigenschaft abgerufen wurde.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Icertcontext:: freecontext-Methode'
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
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367655"
---
# <a name="icertcontextfreecontext-method"></a>Icertcontext:: freecontext-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **freecontext** -Methode gibt einen pccert-kontextfrei, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.

## <a name="syntax"></a>Syntax


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcertcontext* \[ in\]
</dt> <dd>

Der pccert- \_ Kontext, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S \_ OK weist auf Erfolg hin. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt nicht den pccert-kontextfrei, der \_ in einem [**Zertifikat**](certificate.md) Objekt enthalten ist. Es sollte nur verwendet werden, um einen pccert-kontextfrei zugeben, \_ der über die [**certcontext**](icertcontext-certcontext.md) -Eigenschaft abgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icertcontext**](icertcontext.md)
</dt> </dl>

 

 




