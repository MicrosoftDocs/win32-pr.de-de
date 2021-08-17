---
description: Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction::p ut_Completed-Methode
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
ms.openlocfilehash: aff219d5e6847c64034eed1b057e300ea601eedaa8aa7a131f1467aeacc42422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323163"
---
# <a name="iasyncactionput_completed-method"></a>IAsyncAction::p ut \_ Completed-Methode

Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ out\]
</dt> <dd>

Typ: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\***

Die Methode, die die Abschlussbenachrichtigung behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
