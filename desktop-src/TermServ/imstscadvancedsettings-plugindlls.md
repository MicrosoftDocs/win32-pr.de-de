---
title: Imstscadvancedsettings-plugindlls (Eigenschaft)
description: Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Plugindlls-Eigenschaft Remotedesktopdienste
- Plugindlls-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476743"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a>Imstscadvancedsettings::P lugindlls (Eigenschaft)

Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an. Client-DLLs für virtuelle Kanäle werden auch als Plug-in-DLLs bezeichnet.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a>Eigenschaftswert

Durch Trennzeichen getrennte Liste mit den Namen der zu ladenden DLLs des virtuellen Channel-Clients. Die DLL-Namen dürfen nur alphanumerische Zeichen enthalten. Weitere Informationen zum Format dieser Namen finden Sie unter [DVC-Plug-in-Registrierung](dvc-plug-in-registration.md).

## <a name="error-codes"></a>Fehlercodes

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement auf einer Webseite gehostet wird, akzeptiert die **plugindlls** -Eigenschaft aus Sicherheitsgründen nur eine benannte Liste von Client-DLLs für virtuelle Kanäle. Das-Steuerelement gibt einen Fehler zurück, wenn ein Dateisystem oder ein UNC-Pfad angegeben wird.

Virtuelle channelclientdlls, auf die von einer Webseite zugegriffen wird, müssen im Verzeichnis "% windir% \\ system32" installiert sein, da das Remotedesktop ActiveX-Steuerelement nur auf DLL-Dateien an diesem Speicherort zugreift. Wenn das Steuerelement nicht auf einer Webseite gehostet wird, ist diese Sicherheits Einschränkung nicht vorhanden, und vollständige Pfade können verwendet werden, um auf virtuelle channelclientdlls zuzugreifen und Sie zu laden, die sich an beliebiger Stelle im Dateisystem befinden.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





