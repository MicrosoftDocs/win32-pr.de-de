---
title: IMsRdpClientNonScriptable4-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable3-Schnittstelle abgeleitet.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957226"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>IMsRdpClientNonScriptable4-Schnittstelle

Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) -Schnittstelle abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable4** -Schnittstelle erbt von [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable4** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                         | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Allowkredentialsave**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Lesen/Schreiben<br/> | Gibt an, ob im Dialogfeld Anmelde Informationen ein Kontrollkästchen angezeigt wird, um das Speichern von Anmelde Informationen zu aktivieren.<br/>                                                                                        |
| [**Launchedviaclientshellinterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob der Benutzer das Client Steuerelement über die RD-Webzugriff Schnittstelle gestartet hat.<br/>                                                                                                  |
| [**Markrdpsettingssecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Lesen/Schreiben<br/> | Gibt an, ob RDP-Einstellungen als sicher gekennzeichnet sind.<br/>                                                                                                                                          |
| [**Promptforkredsonclient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Lesen/Schreiben<br/> | Gibt an, ob das Client Steuerelement ein Dialogfeld anzeigt, in dem Anmelde Informationen angefordert werden.<br/>                                                                                                      |
| [**Publishercertificatechain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Lesen/Schreiben<br/> | Gibt die Herausgeber Zertifikat Kette an. Die Kette wird in einer Variante vom Typ VT \_ ByRef gespeichert, die einen Zeiger auf eine Struktur der [**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) enthält.<br/> |
| [**Redirectionwarningtype**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Lesen/Schreiben<br/> | Steuert das vorhanden sein und das Erscheinungsbild des Dialog Felds Umleitung.<br/>                                                                                                                           |
| [**Treuhand Website**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Lesen/Schreiben<br/> | Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites des Client Computers enthalten ist.<br/>                                                                |
| [**Warnaboutprinterredirect**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Lesen/Schreiben<br/> | Gibt an, ob das Dialogfeld Umleitung eine Meldung zur Drucker Umleitung anzeigt, bevor eine Sitzung gestartet wird.<br/>                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID \_ MsRdpClient6 ist als 7390f3d8-0439-4c05-91E3-cf5cb290c3d0 definiert.<br/> CLSID- \_ MsRdpClient6NotSafeForScripting ist als D2EA46A7-C2BF-426B-AF24-E19C44456399 definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**Imsrdpclientnonscriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

