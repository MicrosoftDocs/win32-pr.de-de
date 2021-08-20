---
description: Ruft den Transaktions- oder Transaktionsproxy ab, der dem aktuellen Kontext zugeordnet ist(sofern diese dem Kontext zugeordnet ist).
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: IContextTransactionInfo::FetchTransaction-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991060"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>IContextTransactionInfo::FetchTransaction-Methode

Ruft den Transaktions- oder Transaktionsproxy ab, der dem aktuellen Kontext zugeordnet ist(sofern diese dem Kontext zugeordnet ist).

## <a name="syntax"></a>Syntax


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pUnk* \[ out, retval\]
</dt> <dd>

Der Transaktions- oder Transaktionsproxy, der dem aktuellen Kontext zugeordnet ist. andernfalls **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard-Rückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




