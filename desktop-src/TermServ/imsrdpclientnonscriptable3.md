---
title: IMsRdpClientNonScriptable3-Schnittstelle
description: Ermöglicht den Zugriff auf die nicht feststellbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX Steuerelements. Wird von der IMsRdpClientNonScriptable2-Schnittstelle ableiten.
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable3-Remotedesktopdienste
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65756224134392629a11cc0bbe2ef35f8d687cc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474556"
---
# <a name="imsrdpclientnonscriptable3-interface"></a>IMsRdpClientNonScriptable3-Schnittstelle

Ermöglicht den Zugriff auf die nicht feststellbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX Steuerelements. Wird von der [**IMsRdpClientNonScriptable2-Schnittstelle**](imsrdpclientnonscriptable2.md) ableiten. Auf Methoden dieser Schnittstelle kann nur über die vtable zugegriffen werden. Sie sind nicht für skriptfähige Clients verfügbar.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable3-Schnittstelle** erbt von [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md). **IMsRdpClientNonScriptable3** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable3-Schnittstelle** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Lesen/Schreiben<br /> | Die Textzeichenfolge, die für die Verbindungsleiste angezeigt werden soll.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Schreibgeschützt<br /> | Die Sammlung von PnP-Geräten, die für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Schreibgeschützt<br /> | Die Auflistung der Datenträgerlaufwerke, die für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob CredSSP für diese Verbindung aktiviert ist.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die NegotiateSecurityLayer-Einstellung für diese Verbindung unterstützt wird.<br /><blockquote>[!Note]<br />Wenn <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> aktiviert und auf dem Client vorhanden ist, oder wenn Secure Sockets Layer (SSL) mit Benutzerauthentifizierung aktiviert ist, wird NegotiateSecurityLayer ignoriert.</blockquote><br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Eingabeaufforderung für Anmeldeinformationen" angezeigt werden soll.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angeschlossene PnP-Geräte, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob dynamisch angefügte PnP-Laufwerke, die während einer Sitzung aufzählt werden, für die Umleitung verfügbar sind.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Sicherheitswarnung für Umleitung" angezeigt werden soll, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob das Dialogfeld "Sicherheitswarnung" eine Warnung zur Umleitung der Zwischenablage enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lesen/Schreiben<br /> | Gibt an, ob die Sicherheitswarnung eine Warnung zum Senden von Anmeldeinformationen an den Remoteserver enthalten soll, bevor eine Sitzung gestartet wird.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient5 ist als 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 definiert.<br/> CLSID \_ MsRdpClient5NotSafeForScripting ist als 4EB2F086-C818-447E-B32C-C51CE2B30D31 definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 definiert.<br/> CLSID \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





