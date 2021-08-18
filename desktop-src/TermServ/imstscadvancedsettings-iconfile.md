---
title: IMsTscAdvancedSettings IconFile-Eigenschaft
description: Gibt den Namen der Datei mit Symboldaten an, auf die beim Anzeigen des Clients im Vollbildmodus zugegriffen wird.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- IconFile-Eigenschaft Remotedesktopdienste
- IconFile-Eigenschaft Remotedesktopdienste , IMsTscAdvancedSettings-Schnittstelle
- IMsTscAdvancedSettings-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings-Schnittstelle
- IMsRdpClientAdvancedSettings-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , IconFile-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4700c549fa82f932ed12e3f4eeb02f2d557db3f940b394e0f2f875ac6dd7dffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000690"
---
# <a name="imstscadvancedsettingsiconfile-property"></a>IMsTscAdvancedSettings::IconFile-Eigenschaft

Gibt den Namen der Datei mit Symboldaten an, auf die beim Anzeigen des Clients im Vollbildmodus zugegriffen wird.

> [!Note]  
> Diese Eigenschaft wird im ActiveX-Steuerelement (MsRdp.ocx) nicht unterstützt. Sie wird in der MsTscAx.dll Bibliothek unterstützt, die im Standardclient (MsTsc.exe) enthalten ist.

 

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a>Eigenschaftswert

Der vollqualifizierte Pfad der Symboldatei oder einer Datei, die Symboldaten enthält, z. B. eine DLL.

## <a name="error-codes"></a>Fehlercodes

Gibt **S \_ FALSE zurück.**

## <a name="remarks"></a>Hinweise

Die Dateinamenerweiterung einer Symboldatei lautet ".ico".

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | \_IID-IMsTscAdvancedSettings ist als 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d definiert.<br/> |



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

 

 





