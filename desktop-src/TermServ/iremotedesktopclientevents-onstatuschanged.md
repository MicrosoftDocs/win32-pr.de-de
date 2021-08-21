---
title: IRemoteDesktopClientEvents OnStatusChanged-Methode (Locationapi.h)
description: Wird aufgerufen, wenn das Clientsteuerelement seinen Status aktualisiert hat.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- OnStatusChanged-Methode Remotedesktopdienste
- OnStatusChanged-Methode Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnStatusChanged-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08b15eb2b8112afcef6c98a841a249672df2ae3fbb7f36ceea513d53a5b0478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351622"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>IRemoteDesktopClientEvents::OnStatusChanged-Methode

Wird aufgerufen, wenn das Clientsteuerelement seinen Status aktualisiert hat.

## <a name="syntax"></a>Syntax


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*statusCode* 
</dt> <dd>

Der neue Statuscode.

</dd> <dt>

*statusMessage* 
</dt> <dd>

Der Statusmeldungstext.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Locationapi.h</dt> </dl>       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





