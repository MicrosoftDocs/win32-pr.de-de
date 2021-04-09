---
description: Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Status meldet.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>:: Aufrufen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129236"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>:: Aufrufen-Methode

Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Status meldet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*asyncinfo* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[**iasyncoperationwithprogress<TResult, tprogress>**](/previous-versions//br205807(v=vs.85)) \** _

Die asynchrone Aktion, die den Abschluss meldet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iasyncoperationwithprogresscompletedhandler<TResult, tprogress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
