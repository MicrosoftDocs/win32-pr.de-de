---
description: Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: Isuspendingoperation::D eadline-Eigenschaft (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958935"
---
# <a name="isuspendingoperationdeadline-property"></a>Isuspendingoperation::D eadline-Eigenschaft

Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Die verbleibende Zeit bis zum Anhalten eines verzögerten App-Vorgangs.

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

 

 




