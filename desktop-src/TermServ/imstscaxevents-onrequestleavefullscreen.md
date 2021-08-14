---
title: IMsTscAxEvents OnRequestLeaveFullScreen-Methode
description: Wird aufgerufen, wenn der Client an fordert, den Vollbildmodus zu verlassen, und die Eigenschaft IMsTscAdvancedSettings put ContainerHandledFullScreen auf einen Wert ungleich \_ 0 (null) festgelegt wurde.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- OnRequestLeaveFullScreen-Remotedesktopdienste
- OnRequestLeaveFullScreen-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRequestLeaveFullScreen-Methode
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
ms.openlocfilehash: 74f82cd71942f559039a175fdfff9319cae5ea35a73d4698760be4642a23c448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757339"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>IMsTscAxEvents::OnRequestLeaveFullScreen-Methode

Wird aufgerufen, wenn der Client den Vollbildmodus verlassen möchte und die [**Eigenschaft IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) auf einen Wert ungleich 0 (null) festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Im vollbildbasierten Containermodus sollte der Container als Reaktion auf dieses Ereignis den Standard-Vollbildmodus verlassen.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

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

 

 





