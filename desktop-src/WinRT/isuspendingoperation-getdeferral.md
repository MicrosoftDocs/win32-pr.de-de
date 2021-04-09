---
description: Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Isuspendingoperation:: getdeferral-Methode (Windows. applicationmodel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862611"
---
# <a name="isuspendingoperationgetdeferral-method"></a>Isuspendingoperation:: getdeferral-Methode

Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verzögerung* \[ Out, retval\]
</dt> <dd>

Die Unterbrechung der Verzögerung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Isuspendingoperation**](isuspendingoperation.md)
</dt> </dl>

 

 




