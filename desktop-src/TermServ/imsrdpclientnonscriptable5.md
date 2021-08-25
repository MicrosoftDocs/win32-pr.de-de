---
title: IMsRdpClientNonScriptable5-Schnittstelle
description: Ermöglicht den Zugriff auf die nicht beschreibbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable4-Schnittstelle abgeleitet.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb7f3407f0dc6b1bc8dc04c6c4a72cda95db6b6b1def088a18908a730b96600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009800"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>IMsRdpClientNonScriptable5-Schnittstelle

Ermöglicht den Zugriff auf die nicht beschreibbaren Eigenschaften der Remotesitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable4-Schnittstelle**](imsrdpclientnonscriptable4.md) abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die vtable zugegriffen werden. Sie sind nicht für die Verwendung für skriptfähige Clients verfügbar.

Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**IMsTscAx-Objekt**](imstscax-interface.md) abgerufen, wobei **\_ IID-IMsRdpClientNonScriptable5** übergeben werden.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable5-Schnittstelle** erbt von [**IMsRdpClientNonScriptable4.**](imsrdpclientnonscriptable4.md) **IMsRdpClientNonScriptable5** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable5-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                         | Zugriffstyp           | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Lesegeschützt<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungsleiste deaktivieren soll.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Schreibgeschützt<br/>  | Gibt das umgrenzende Rechteck des Remotemonitors an.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Schreibgeschützt<br/>  | Gibt die Anzahl der Remotemonitore an.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Remotemonitorlayout mit dem Layout des lokalen Monitors identisch ist.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht verwendet.<br/>                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54D38BF7-B1EF-4479-9674-1BD6EA465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5F681803-2900-4C43-A1CC-CF405404A676 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301B94BA-5D25-4A12-BFFE-3B6E7A616585 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | \_IID-IMsRdpClientNonScriptable5 ist als 4f6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

