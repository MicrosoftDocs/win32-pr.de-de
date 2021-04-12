---
description: Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Iasyncaction:: get_Completed-Methode'
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
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129240"
---
# <a name="iasyncactionget_completed-method"></a>Iasyncaction:: get- \_ Methode abgeschlossen

Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **asyncactioncompletedhandler**](asyncactioncompletedhandler.md)\*\***

Die Methode, die die Abschluss Benachrichtigung behandelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

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

 

 
