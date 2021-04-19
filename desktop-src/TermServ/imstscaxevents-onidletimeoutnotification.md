---
title: Imstscaxevents-Methode (onidletimeoutnotification)
description: Wird aufgerufen, wenn der Benutzer während der von der imsrdpclientadvancedsettings Put minutestoidletimeout-Methode festgelegten Zeitspanne keine Maus-oder Tastatureingaben eingegeben hat \_ .
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Onidletimeoutnotification-Methode Remotedesktopdienste
- Onidletimeoutnotification-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onidletimeoutnotification-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346725"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Imstscaxevents:: onidletimeoutnotification-Methode

Wird aufgerufen, wenn der Benutzer während der von der [**imsrdpclientadvancedsettings::p UT \_ minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) -Methode festgelegten Zeitspanne keine Maus-oder Tastatureingaben hat.

## <a name="syntax"></a>Syntax


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist der Wert der [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) -Eigenschaft auf 0 (null) festgelegt, und das System überwacht keine Leerlauf Timeouts. Dieses Ereignis tritt nur auf, wenn die-Eigenschaft auf einen Wert ungleich 0 (null) festgelegt ist.

Der Wert von [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) wird automatisch zurückgesetzt, wenn das Ereignis eintritt.

Anwendungen können [**minutestoidletimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in Situationen verwenden, in denen es nützlich ist, einen Benutzer zu trennen. beispielsweise in einem Kiosk oder einem anderen Szenario mit öffentlichem Terminal.

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

 

 





