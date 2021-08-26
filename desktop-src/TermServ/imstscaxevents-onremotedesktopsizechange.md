---
title: IMsTscAxEvents OnRemoteDesktopSizeChange-Methode
description: Wird aufgerufen, um anzugeben, dass sich die Größe des Clientsteuer steuerelements auf dem Remotedesktop als Reaktion auf einen Clientsteuerungsvorgang geändert hat.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- OnRemoteDesktopSizeChange-Remotedesktopdienste
- OnRemoteDesktopSizeChange-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRemoteDesktopSizeChange-Methode
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
ms.openlocfilehash: 316b70c3405c13dd50c773d36c20f036c9e99aebeb3e5dedae692c2f9ad772fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125090"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>IMsTscAxEvents::OnRemoteDesktopSizeChange-Methode

Wird aufgerufen, um anzugeben, dass sich die Größe des Clientsteuer steuerelements auf dem Remotedesktop als Reaktion auf einen Clientsteuerungsvorgang geändert hat.

## <a name="syntax"></a>Syntax


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*width* \[ In\]
</dt> <dd>

Breite des Remotedesktops mit geänderter Größe in Pixel.

</dd> <dt>

*height* \[ In\]
</dt> <dd>

Höhe des Remotedesktops mit geänderter Größe in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Ereignis ermöglicht dem Container zu bestimmen, ob er sich selbst als Reaktion auf einen Clientsteuerungsvorgang ändern muss, was zu einer größeren anzeigebaren Desktopgröße führen kann. Beachten Sie, dass das Steuerelement automatisch Scrollleisten für die neue Sitzungsgröße an passt.

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

 

 





