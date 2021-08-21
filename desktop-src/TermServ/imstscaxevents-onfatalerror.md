---
title: IMsTscAxEvents OnFatalError-Methode
description: Wird aufgerufen, wenn beim Clientsteuerelement ein schwerwiegender Fehler auftritt.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- OnFatalError-Methode Remotedesktopdienste
- OnFatalError-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnFatalError-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a10315eca4fcbf96edf123699614d29a2c0b8974f563c52148b5de75310fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000680"
---
# <a name="imstscaxeventsonfatalerror-method"></a>IMsTscAxEvents::OnFatalError-Methode

Wird aufgerufen, wenn beim Clientsteuerelement ein schwerwiegender Fehler auftritt.

## <a name="syntax"></a>Syntax


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errorCode* \[ In\]
</dt> <dd>

Gibt den Fehlercode an.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Es ist ein unbekannter Fehler aufgetreten.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Interner Fehlercode 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Es ist ein Fehler mit nicht genügend Arbeitsspeicher aufgetreten.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Es ist ein Fehler bei der Fenstererstellung aufgetreten.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Interner Fehlercode 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

Interner Fehlercode 3. Dies ist kein gültiger Zustand.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6**


</dt> <dd>

Interner Fehlercode 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Während der Clientverbindung ist ein nicht behebbarer Fehler aufgetreten.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Winsock-Initialisierungsfehler.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Als Reaktion auf dieses Ereignis zeigt der Container eine Fehlermeldung an und wird heruntergefahren.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





