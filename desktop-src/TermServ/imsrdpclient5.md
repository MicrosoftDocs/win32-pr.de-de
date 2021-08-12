---
title: IMsRdpClient5-Schnittstelle
description: Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der IMsRdpClient4-Schnittstelle ableiten.
ms.assetid: d3fc5e67-f4d9-4d80-b572-8fc3e660571e
ms.tgt_platform: multiple
keywords:
- IMsRdpClient5-Remotedesktopdienste
- IMsRdpClient5-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7948d402219faa930ddc9087af1ba387bde3ce8d70752fd842a364e85b41abb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609291"
---
# <a name="imsrdpclient5-interface"></a>IMsRdpClient5-Schnittstelle

Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der [**IMsRdpClient4-Schnittstelle**](imsrdpclient4.md) ableiten.

## <a name="members"></a>Member

Die **IMsRdpClient5-Schnittstelle** erbt von [**IMsRdpClient4**](imsrdpclient4.md). **IMsRdpClient5** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient5-Schnittstelle** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------|
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) | Ruft die Fehlercodes und Fehlermeldungen ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient5-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp          | BESCHREIBUNG                                                                                         |
|:------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------|
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/> | Schreibgeschützt<br/> | Die Schnittstelle zu [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).<br/> |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>   | Schreibgeschützt<br/> | Die Clienteinstellungen für das Webportal-Startfeld.<br/>                                         |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>         | Schreibgeschützt<br/> | Die RemoteApp-Clienteinstellung.<br/>                                                            |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/> | Schreibgeschützt<br/> | Die Client-RD-Gatewayeinstellung.<br/>                                                           |



 

## <a name="remarks"></a>Hinweise

Die **IMsRdpClient5-Schnittstelle** wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-b922-e06a28ecd8bf definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





