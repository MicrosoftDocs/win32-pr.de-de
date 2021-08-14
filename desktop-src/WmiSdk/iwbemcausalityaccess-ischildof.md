---
description: Die IsChildOf-Methode bestimmt, ob eine Anforderung ein untergeordnetes Teil einer angegebenen Anforderung (pId) ist.
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: IWbemCausalityAccess::IsChildOf-Methode (Wbemint.h)
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
ms.openlocfilehash: 509508d5e1a273dc681cf3c9f645ead1037408d6ecfe5ed666186ba6e2a2c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318292"
---
# <a name="iwbemcausalityaccessischildof-method"></a>IWbemCausalityAccess::IsChildOf-Methode

Die **IsChildOf-Methode** bestimmt, ob eine Anforderung ein untergeordnetes Teil einer angegebenen Anforderung (pId) ist. Eine übergeordnete Anforderung kann mehrere untergeordnete Anforderungen haben. Jede Anforderung wird durch einen Globally Unique Identifier (GUID) identifiziert und kann über eine übergeordnete Anforderung verfügen oder eine oberste Anforderung sein. Eine GUID ist eine eindeutige 128-Bit-Zahl.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ In\]
</dt> <dd>

Der GUID-Wert, der eine Anforderung eindeutig identifiziert. Beispiel: 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt erfolgreich zurück, wenn die angegebene Anforderung ein untergeordnetes Teil der Anforderung ist, die die **IsChildOf-Methode** aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




