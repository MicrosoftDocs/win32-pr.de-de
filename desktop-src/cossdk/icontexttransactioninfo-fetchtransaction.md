---
description: Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Icontexttransaktioninfo:: fetchtransaction-Methode'
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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127032"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Icontexttransaktioninfo:: fetchtransaction-Methode

Ruft ggf. den Transaktions-oder Transaktions Proxy ab, der dem aktuellen Kontext zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* \[ Out, retval\]
</dt> <dd>

Der Transaktions-oder Transaktions Proxy, der dem aktuellen Kontext zugeordnet ist. andernfalls **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory, e \_ unerwartet und S OK zurückgeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontexttransaktioninfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




