---
title: IMsRdpClient10-Schnittstelle
description: Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der IMsRdpClient9-Schnittstelle ableiten.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- IMsRdpClient10-Remotedesktopdienste
- IMsRdpClient10-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737240"
---
# <a name="imsrdpclient10-interface"></a>IMsRdpClient10-Schnittstelle

Stellt die Methoden und Eigenschaften zur Konfiguration und Verwendung des Clientsteuer steuerelements zur Anwendung. Wird von der [**IMsRdpClient9-Schnittstelle**](imsrdpclient9.md) ableiten.

## <a name="members"></a>Member

Die **IMsRdpClient10-Schnittstelle** erbt von [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient10-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**Attachevent**](imsrdpclient9-attachevent.md)                                   | Angefügt ein Ereignis.<br/>                                                       |
| [**Detachevent**](imsrdpclient9-detachevent.md)                                   | Trennt ein Ereignis.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Ruft die Fehlerbeschreibung für die Sitzungstrennungsereignisse ab.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Ruft den Statustext für den angegebenen Statuscode ab.<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Ruft die für einen virtuellen Kanal festgelegten Optionen ab.<br/>                         |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                       | Verbindet sich mit der neuen Desktopbreite und -höhe erneut mit der Remotesitzung.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX an.<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Bewirkt, dass eine Aktion in der Remotesitzung ausgeführt wird.<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Legt die Optionen für den virtuellen Kanal für das Remotedesktop ActiveX fest.<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronisiert Einstellungen für die Sitzungsanzeige.<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aktualisiert einstellungen für die Sitzungsanzeige.<br/>                                        |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient10-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | Beschreibung                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings-Schnittstelle**](imsrdpclientadvancedsettings-interface.md) ab. Die -Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Clientsteuersystem zu festlegen.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2-Schnittstelle**](imsrdpclientadvancedsettings2.md) ab. Die -Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Clientsteuersystem zu festlegen.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings3-Schnittstelle**](imsrdpclientadvancedsettings3.md) ab.<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4-Schnittstelle**](imsrdpclientadvancedsettings4.md) ab.<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings5-Schnittstelle**](imsrdpclientadvancedsettings5.md) ab.<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings6-Schnittstelle**](imsrdpclientadvancedsettings5.md) ab.<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientAdvancedSettings7-Schnittstelle**](imsrdpclientadvancedsettings7.md) unterstützt.<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Schreibgeschützt<br/>  | Enthält ein -Objekt, das die [**IMsRdpClientAdvancedSettings8-Schnittstelle**](imsrdpclientadvancedsettings8.md) unterstützt.<br/>                                                                          |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Die Farbtiefe (in Bits pro Pixel) für die Verbindung des Steuerelements.<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Enthält den Text, der im Clientbereich des Steuerelements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Enthält erweiterte Informationen zum Grund für die Trennung der Verbindung des Steuerelements.<br/>                                                                                                                     |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Bestimmt, ob sich das Clientsteuer steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Schreibgeschützt<br/>  | Ruft die skriptfähige Clienteinstellungsschnittstelle [**IMsRdpClientShell ab.**](imsrdpclientshell.md)<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram-Schnittstelle**](itsremoteprogram.md) unterstützt.<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram2-Schnittstelle**](itsremoteprogram2.md) unterstützt.<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Schreibgeschützt<br/>  | Ein Objekt, das die [**ITSRemoteProgram3-Schnittstelle**](itsremoteprogram3.md) unterstützt.<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientSecuredSettings-Schnittstelle**](imsrdpclientsecuredsettings-interface.md) ab. Diese Schnittstelle kann verwendet werden, um gesicherte Einstellungen für das Clientsteuer steuerelement zu festlegen.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2-Schnittstelle**](imsrdpclientsecuredsettings2.md) unterstützt.<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Schreibgeschützt<br/>  | Ruft ab, was über ein Skript an die [**IMsRdpClientTransportSettings-Schnittstelle übergeben**](imsrdpclienttransportsettings.md) wurde.<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientTransportSettings2-Schnittstelle**](imsrdpclienttransportsettings2.md) ab.<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3-Schnittstelle**](imsrdpclienttransportsettings3.md) unterstützt.<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4-Schnittstelle**](imsrdpclienttransportsettings4.md) unterstützt.<br/>                                                                       |



 

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 ist als 7ED92C39-EB38-4927-A70A-708AC5A59321 definiert.<br/>                                                                                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

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

 

