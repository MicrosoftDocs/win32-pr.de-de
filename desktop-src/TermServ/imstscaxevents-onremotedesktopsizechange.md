---
title: Imstscaxevents onremotedesktopsizechange-Methode
description: Wird aufgerufen, um anzugeben, dass sich die Größe des Client Steuer Elements auf dem Remote Desktop als Reaktion auf einen Client Steuerungs Vorgang geändert hat.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Onremotedesktopsizechange-Methode Remotedesktopdienste
- Onremotedesktopsizechange-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremotedesktopsizechange-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518053"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>Imstscaxevents:: onremotedesktopsizechange-Methode

Wird aufgerufen, um anzugeben, dass sich die Größe des Client Steuer Elements auf dem Remote Desktop als Reaktion auf einen Client Steuerungs Vorgang geändert hat.

## <a name="syntax"></a>Syntax


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ in\]
</dt> <dd>

Breite der Größe des Remote Desktops in Pixel.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Höhe der Größe des Remote Desktops in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ermöglicht dem Container festzustellen, ob seine Größe als Reaktion auf einen Client Steuerungs Vorgang geändert werden muss. Dies kann zu einer größeren sichtbaren Desktop Größe führen. Beachten Sie, dass das Steuerelement Scrollleisten automatisch für die neue Sitzungs Größe anpasst.

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

 

 





