---
description: Benachrichtigt das System, dass die App ihre Daten gespeichert hat und angehalten werden kann.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: ISuspendingDeferral::Complete-Methode (Windows. ApplicationModel.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 8fb16ae67ad5dcd9324c176a39a0dc9e566638ed960443496a0d556990bd8717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464400"
---
# <a name="isuspendingdeferralcomplete-method"></a>ISuspendingDeferral::Complete-Methode

Benachrichtigt das System, dass die App ihre Daten gespeichert hat und angehalten werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 




