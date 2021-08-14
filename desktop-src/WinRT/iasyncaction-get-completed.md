---
description: Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: IAsyncAction::get_Completed-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 90e26947f0771490334ee731b25576759943c44cc47a9fda6681da9aa1f11fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323441"
---
# <a name="iasyncactionget_completed-method"></a>IAsyncAction::get \_ Completed-Methode

Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ out\]
</dt> <dd>

Typ: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

Die Methode, die die Abschlussbenachrichtigung behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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

 

 
