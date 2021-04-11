---
description: Ruft den Vorgang zum Anhalten der App ab.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Isuspendingeventargs:: suspendingoperation-Eigenschaft (Windows. applicationmodel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862612"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a>Isuspendingeventargs:: suspendingoperation (Eigenschaft)

Ruft den Vorgang zum Anhalten der App ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der anhalten-Vorgang.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Isuspendingeventargs**](isuspendingeventargs.md)
</dt> </dl>

 

 




