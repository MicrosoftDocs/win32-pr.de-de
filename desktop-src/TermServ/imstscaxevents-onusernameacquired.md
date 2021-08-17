---
title: IMsTscAxEvents OnUserNameAcquired-Methode
description: Wird aufgerufen, wenn der Benutzername vom Steuerelement abgerufen wurde.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- OnUserNameAcquired-Methode Remotedesktopdienste
- OnUserNameAcquired-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnUserNameAcquired-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05b63d59ebe0610b28198d264caf0fb7d3cd87f9ee664f804dc38eb2996abd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757153"
---
# <a name="imstscaxeventsonusernameacquired-method"></a>IMsTscAxEvents::OnUserNameAcquired-Methode

Wird aufgerufen, wenn der Benutzername vom Steuerelement abgerufen wurde.

## <a name="syntax"></a>Syntax


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrUserName* 
</dt> <dd>

Der Benutzername.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





