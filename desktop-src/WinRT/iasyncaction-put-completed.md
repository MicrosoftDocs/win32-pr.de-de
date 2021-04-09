---
description: Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: Iasyncaction::p ut_Completed-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958937"
---
# <a name="iasyncactionput_completed-method"></a>Iasyncaction: Abgeschlossene:p UT- \_ Methode

Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **[**asyncactioncompletedhandler**](asyncactioncompletedhandler.md) \** _

Die Methode, die die Abschluss Benachrichtigung behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
