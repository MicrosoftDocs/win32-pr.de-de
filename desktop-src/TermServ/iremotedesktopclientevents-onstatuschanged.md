---
title: Iremotedesktopclientevents-Methode (locationapi. h)
description: Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Onstatuschangi-Methode Remotedesktopdienste
- Onstatuschangimethode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onstatuschangi-Methode
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
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478879"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a>Iremotedesktopclientevents:: onstatuschangi-Methode

Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.

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

Der Text der Statusmeldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Locationapi. h</dt> </dl>       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclientevents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





