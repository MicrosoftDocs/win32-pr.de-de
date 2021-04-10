---
description: Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'Asyncactioncompletedhandler:: Aufrufen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129248"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a>Asyncactioncompletedhandler:: Aufrufen-Methode

Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*asyncinfo* \[ in\]
</dt> <dd>

Typ: **[**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _

Die asynchrone Aktion, die den Abschluss meldet.

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

[**Asyncactioncompletedhandler**](asyncactioncompletedhandler.md)
</dt> </dl>

 

