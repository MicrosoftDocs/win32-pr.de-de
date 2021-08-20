---
title: IMsRdpClientNonScriptable2-Schnittstelle
description: Ermöglicht den Zugriff auf die nicht feststellbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX Steuerelement. Wird von der IMsRdpClientNonScriptable-Schnittstelle ableiten.
ms.assetid: 06a5ffc9-3c9e-44d6-a5b5-9ccb7488deff
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable2-Remotedesktopdienste
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77df65d58ad2c3b479cac37a9ae543733d4c8c90bd4708c5e6e0273fcb142ae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352137"
---
# <a name="imsrdpclientnonscriptable2-interface"></a>IMsRdpClientNonScriptable2-Schnittstelle

Ermöglicht den Zugriff auf die nicht feststellbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX Steuerelement. Wird von der [**IMsRdpClientNonScriptable-Schnittstelle**](imsrdpclientnonscriptable-interface.md) ableiten. Auf Methoden dieser Schnittstelle kann nur über die vtable zugegriffen werden. Sie sind nicht für skriptfähige Clients verfügbar.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable2-Schnittstelle** erbt von [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md). **IMsRdpClientNonScriptable2** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | Beschreibung                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lesen/Schreiben<br/> | Das Fensterhand handle, das als übergeordnetes Fenster für das Steuerelement verwendet werden soll. Dadurch können alle fenster, die vom -Steuerelement angezeigt werden, in Bezug auf alle fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008, Windows Server 2008 mit SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient4 ist als 4EDCB26C-D24C-4E72-AF07-B576699AC0DE definiert.<br/> CLSID \_ MsRdpClient4a ist als 54CE37E0-9834-41AE-9896-4DAB69DC022B definiert.<br/> CLSID \_ MsRdpClient4NotSafeForScripting ist als 6AE29350-321B-42BE-BBE5-12FB5270C0DE definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 ist als 17A5E535-4072-4FA4-AF32-C8D0D47345E9 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





