---
title: IMsTscAdvancedSettings-Plug-InDlls (Eigenschaft)
description: Gibt die Namen der zu ladenden Client-DLLs des virtuellen Kanals an.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- PluginDlls-Remotedesktopdienste
- PluginDlls-Remotedesktopdienste , IMsTscAdvancedSettings-Schnittstelle
- IMsTscAdvancedSettings-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
- PluginDlls-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , PluginDlls-Eigenschaft
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
ms.openlocfilehash: e896a8ce82a6e1dee7896a242bb2dace442dba595a66a7c45a7c3baf3060dff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606131"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a>IMsTscAdvancedSettings::P luginDlls-Eigenschaft

Gibt die Namen der zu ladenden Client-DLLs des virtuellen Kanals an. Client-DLLs für virtuelle Kanäle werden auch als Plug-In-DLLs bezeichnet.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a>Eigenschaftswert

Durch Komma getrennte Liste der Namen der zu ladenden Client-DLLs des virtuellen Kanals. Die DLL-Namen dürfen nur alphanumerische Zeichen enthalten. Weitere Informationen zum Format dieser Namen finden Sie unter [DVC-Plug-In-Registrierung.](dvc-plug-in-registration.md)

## <a name="error-codes"></a>Fehlercodes

Geben Sie **S \_ OK zurück,** falls erfolgreich.

## <a name="remarks"></a>Hinweise

Aus Sicherheitsgründen akzeptiert die **PluginDlls-Eigenschaft** nur eine benannte Liste von Client-DLLs für virtuelle Kanäle, wenn das Steuerelement auf einer Webseite gehostet wird. Das Steuerelement gibt einen Fehler zurück, wenn ein Dateisystem oder ein UNC-Pfad angegeben ist.

Client-DLLs für virtuelle Kanäle, auf die von einer Webseite aus zugegriffen wird, müssen im Verzeichnis "%WinDir% system32" installiert werden, da das Remotedesktop ActiveX-Steuerelement nur auf DLL-Dateien an diesem Speicherort \\ zusteuert. Wenn das Steuerelement nicht auf einer Webseite gehostet wird, ist diese Sicherheitseinschränkung nicht vorhanden, und vollständige Pfade können verwendet werden, um auf Client-DLLs für virtuelle Kanäle zu zugreifen und diese zu laden, die sich an einer beliebigen Stelle im Dateisystem befinden.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings ist als 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





