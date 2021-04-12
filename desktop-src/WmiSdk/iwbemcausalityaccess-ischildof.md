---
description: Die ischildof-Methode bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen Anforderung (pId) ist.
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Iwbemkausalityaccess:: ischildof-Methode (wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217119"
---
# <a name="iwbemcausalityaccessischildof-method"></a>Iwbemkausalityaccess:: ischildof-Methode

Die **ischildof** -Methode bestimmt, ob eine Anforderung ein untergeordnetes Element einer angegebenen Anforderung (pId) ist. Eine übergeordnete Anforderung kann über mehrere untergeordnete Anforderungen verfügen. Jede Anforderung wird durch einen global eindeutigen Bezeichner (GUID) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine Top-Anforderung sein. Eine GUID ist eine eindeutige 128-Bit-Zahl.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ in\]
</dt> <dd>

Der GUID-Wert, der eine Anforderung eindeutig identifiziert. Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt erfolgreich zurück, wenn die angegebene Anforderung ein untergeordnetes Element der Anforderung ist, die die **ischildof** -Methode aufgerufen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwbemkausalityaccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




