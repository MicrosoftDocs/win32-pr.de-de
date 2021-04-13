---
title: Imsrdpclientsecuredsettings audioredirectionmode-Eigenschaft
description: Gibt die audioumleitungs Einstellungen an, die angeben, ob Sounds oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) umgeleitet werden sollen.
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Audioredirectionmode-Eigenschaft Remotedesktopdienste
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, audioredirectionmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519228"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>Imsrdpclientsecuredsettings:: audioredirectionmode-Eigenschaft

Gibt die audioumleitungs Einstellungen an, die angeben, ob Sounds oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) umgeleitet werden sollen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Eigenschaftswert

Die neuen Einstellungen. Dieser Parameter kann einen der folgenden Werte annehmen.

<dt>

0
</dt> <dd>

Umleiten von Sounds an den Client. Dies ist der Standardwert.

</dd> <dt>

1
</dt> <dd>

Abspielen von Sounds auf dem Remote Computer.

</dd> <dt>

2
</dt> <dd>

Sound Umleitung deaktivieren; Spielen Sie keine Sounds auf dem Server.

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





