---
title: Imstscaxevents onfatalerror-Methode
description: Wird aufgerufen, wenn das Client Steuerelement einen schwerwiegenden Fehler feststellt.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Onfatalerror-Methode Remotedesktopdienste
- Onfatalerror-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onfatalerror-Methode
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
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859032"
---
# <a name="imstscaxeventsonfatalerror-method"></a>Imstscaxevents:: onfatalerror-Methode

Wird aufgerufen, wenn das Client Steuerelement einen schwerwiegenden Fehler feststellt.

## <a name="syntax"></a>Syntax


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errorCode* \[ in\]
</dt> <dd>

Gibt den Fehlercode an.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Ein unbekannter Fehler ist aufgetreten.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Interner Fehlercode 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Fehler aufgrund von nicht genügend Arbeitsspeicher.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Ein Fenster Erstellungs Fehler ist aufgetreten.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Interner Fehlercode 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5@@**


</dt> <dd>

Interner Fehlercode 3. Dies ist kein gültiger Status.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6**


</dt> <dd>

Interner Fehlercode 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**19.00**


</dt> <dd>

Nicht BEHEB barer Fehler während der Client Verbindung.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Winsock-Initialisierungsfehler.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Als Reaktion auf dieses Ereignis zeigt der Container eine Fehlermeldung an und wird heruntergefahren.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





