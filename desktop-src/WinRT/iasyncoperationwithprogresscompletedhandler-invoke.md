---
description: Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Fortschritt meldet.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke-Methode
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
ms.openlocfilehash: 141f79398e1f9f250b402df130daa728c8e2f0e5f78702d7866dbe9a202b5978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323119"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke-Methode

Ruft die Methode auf, die aufgerufen wird, wenn der angegebene asynchrone Vorgang den Fortschritt meldet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*asyncInfo* \[ In\]
</dt> <dd>

Typ: **[ **IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\***

Die asynchrone Aktion, die den Abschluss meldet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
