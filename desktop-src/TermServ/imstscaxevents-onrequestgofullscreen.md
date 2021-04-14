---
title: Imstscaxevents onrequestgofullscreen-Methode
description: Wird aufgerufen, wenn der Client anfordert, in den Vollbildmodus zu wechseln, und die imstscadvancedsettings put \_ containerhandledfullscreen-Methode aufgerufen wird, um die containerhandledfullscreen-Eigenschaft auf einen Wert ungleich 0 (null) festzulegen.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Onrequestgofullscreen-Methode Remotedesktopdienste
- Onrequestgofullscreen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestgofullscreen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392021"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>Imstscaxevents:: onrequestgofullscreen-Methode

Wird aufgerufen, wenn der Client anfordert, in den Vollbildmodus zu wechseln, und die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Methode aufgerufen wird, um die **containerhandledfullscreen** -Eigenschaft auf einen Wert ungleich 0 (null) festzulegen.

## <a name="syntax"></a>Syntax


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Im Container behandelten Vollbildmodus sollte der Container als Reaktion auf dieses Ereignis den Standardmodus für den Vollbildmodus eingeben.

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

 

 





