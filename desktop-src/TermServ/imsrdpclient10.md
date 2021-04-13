---
title: IMsRdpClient10-Schnittstelle
description: Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der IMsRdpClient9-Schnittstelle abgeleitet.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- IMsRdpClient10-Schnittstelle Remotedesktopdienste
- IMsRdpClient10 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: a5992803a04a771aed716251bd25ca2eceb9f94d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391681"
---
# <a name="imsrdpclient10-interface"></a>IMsRdpClient10-Schnittstelle

Stellt die Methoden und Eigenschaften bereit, die zum Konfigurieren und Verwenden des Client Steuer Elements erforderlich sind. Wird von der [**IMsRdpClient9**](imsrdpclient9.md) -Schnittstelle abgeleitet.

## <a name="members"></a>Member

Die **IMsRdpClient10** -Schnittstelle erbt von [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClient10** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**"AttachEvent"**](imsrdpclient9-attachevent.md)                                   | Fügt ein Ereignis an.<br/>                                                       |
| [**DetachEvent**](imsrdpclient9-detachevent.md)                                   | Trennt ein Ereignis.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Ruft die Fehlerbeschreibung für die Sitzungs Trennungs Ereignisse ab.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Ruft den Status Text für den angegebenen Statuscode ab.<br/>                 |
| [**Getvirtualchanneloptions**](imsrdpclient-getvirtualchanneloptions.md)          | Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.<br/>                         |
| [**Verbindung wiederherstellen**](imsrdpclient8-reconnect.md)                                       | Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an.<br/>      |
| [**Sendremoteaction**](imsrdpclient8-sendremoteaction.md)                         | Bewirkt, dass eine Aktion in der Remote Sitzung ausgeführt wird.<br/>                  |
| [**Setvirtualchanneloptions**](imsrdpclient-setvirtualchanneloptions.md)          | Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.<br/> |
| [**Syncsessiondisplaysettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Synchronisiert Sitzungs Anzeigeeinstellungen.<br/>                                   |
| [**Updatesessiondisplaysettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aktualisiert die Sitzungs Anzeigeeinstellungen.<br/>                                        |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClient10** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle ab.<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Schreibgeschützt<br/>  | Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) -Schnittstelle ab.<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstelle unterstützt.<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Schreibgeschützt<br/>  | Enthält ein Objekt, das die [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) -Schnittstelle unterstützt.<br/>                                                                          |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lesen/Schreiben<br/> | Die Farbtiefe (in Bits pro Pixel) für die Verbindung des-Steuer Elements.<br/>                                                                                                                               |
| [**Connectedstatustext**](imsrdpclient2-connectedstatustext.md)<br/>          | Lesen/Schreiben<br/> | Enthält den Text, der im Client Bereich des-Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.<br/>                                                                              |
| [**Extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md)<br/> | Schreibgeschützt<br/>  | Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.<br/>                                                                                                                     |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lesen/Schreiben<br/> | Bestimmt, ob sich das Client Steuerelement im Vollbildmodus befindet.<br/>                                                                                                                                   |
| [**Msrdpclientshell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Schreibgeschützt<br/>  | Ruft die Skript fähige-Client Einstellungs Schnittstelle [**imsrdpclientshell**](imsrdpclientshell.md)ab.<br/>                                                                                               |
| [**Remoteprogram**](imsrdpclient5-remoteprogram.md)<br/>                      | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**itsremoteprogram**](itsremoteprogram.md) -Schnittstelle unterstützt.<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**ITSRemoteProgram2**](itsremoteprogram2.md) -Schnittstelle unterstützt.<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Schreibgeschützt<br/>  | Ein Objekt, das die [**ITSRemoteProgram3**](itsremoteprogram3.md) -Schnittstelle unterstützt.<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Schreibgeschützt<br/>  | Ruft einen Zeiger auf die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle ab. Diese Schnittstelle kann verwendet werden, um gesicherte Einstellungen für das Client Steuerelement festzulegen.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) -Schnittstelle unterstützt.<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Schreibgeschützt<br/>  | Ruft ab, was durch ein Skript an die [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstelle übermittelt wurde.<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Schreibgeschützt<br/>  | Ruft die [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) -Schnittstelle ab.<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstelle unterstützt.<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Schreibgeschützt<br/>  | Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) -Schnittstelle unterstützt.<br/>                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 ist als 7ed92c39-EB38-4927-a70a-708ac5a59321 definiert<br/>                                                                                                        |



## <a name="see-also"></a>Siehe auch

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

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

