---
title: Imstscsecuredsettings-FullScreen-Eigenschaft
description: Gibt den voll Bild Zustand des Client Steuer Elements an.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Voll Bildeigenschaften Remotedesktopdienste
- Voll Bildeigenschaften Remotedesktopdienste, imstscsecuredsettings-Schnittstelle
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
- Voll Bildeigenschaften Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, FullScreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341028"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>Imstscsecuredsettings:: FullScreen-Eigenschaft

Gibt den voll Bild Zustand des Client Steuer Elements an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Eigenschaftswert

Legen Sie diesen Parameter auf **true** fest, wenn das Steuerelement den Vollbildmodus verwenden soll, und andernfalls **false** .

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu dieser Methode finden Sie unter [Bereitstellen von RDP-Client Sicherheit](providing-for-rdp-client-security.md).

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

Beachten Sie Folgendes: Obwohl die Verwendung dieser Eigenschaft auf die zulässigen Internet Explorer-URL-Sicherheitszonen beschränkt ist, kann ein Benutzer jederzeit in den Vollbildmodus wechseln, nachdem die Verbindung hergestellt wurde, indem er die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus gedrückt hat (Strg + Alt + untbuggung).

Diese Methode kann aufgerufen werden, während die Client Verbindung hergestellt wird.

Sie müssen die [**IMsRdpClientNonScriptable3::p UT \_ connectionbartext**](imsrdpclientnonscriptable3-connectionbartext.md) -Methode anrufen, bevor Sie die **imstscsecuredsettings::p UT- \_ voll Bild** Methode oder die [**imsrdpclient::p UT- \_ voll Bild**](imsrdpclient-fullscreen.md) Methode aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ imstscsecuredsettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**Imstscsecuredsettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





