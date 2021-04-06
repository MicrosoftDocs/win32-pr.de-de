---
title: Imstscaxevents onrequestleavefullscreen-Methode
description: Wird aufgerufen, wenn der Client anfordert, den Vollbildmodus zu verlassen, und die imstscadvancedsettings put \_ containerhandledfullscreen-Eigenschaft auf einen Wert ungleich 0 (null) festgelegt wurde.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Onrequestleavefullscreen-Methode Remotedesktopdienste
- Onrequestleavefullscreen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestleavefullscreen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742096"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>Imstscaxevents:: onrequestleavefullscreen-Methode

Wird aufgerufen, wenn der Client den Vollbildmodus verlässt und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Eigenschaft auf einen Wert ungleich 0 (null) festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Im Container behandelten Vollbildmodus sollte der Container den Standard-Vollbildmodus als Reaktion auf dieses Ereignis belassen.

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

 

 





