---
title: IMsRdpClientShell-Schnittstelle
description: Remotedesktopverbindung Clienteinstellungen (RDC), die zum Starten des Clients über Remotedesktop Webzugriff (RD Webzugriff) oder über andere Webportale verwendet werden.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell-Remotedesktopdienste
- IMsRdpClientShell-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8593a890097bbfaf6d9c9876bb56d92794ce204f38f349c72beb73b8d28403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621030"
---
# <a name="imsrdpclientshell-interface"></a>IMsRdpClientShell-Schnittstelle

Remotedesktopverbindung Clienteinstellungen (RDC), die zum Starten des Clients über Remotedesktop Webzugriff (RD Webzugriff) oder über andere Webportale verwendet werden.

## <a name="members"></a>Member

Die **IMsRdpClientShell-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientShell** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IMsRdpClientShell-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | Beschreibung                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Ruft eine einzelne RDP-Eigenschaft ab.<br/>                  |
| [**Starten**](imsrdpclientshell-launch.md)                 | Startet remoten Dateiinhalt über das Webportal.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Legt eine einzelne RDP-Eigenschaft fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientShell-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                              | Zugriffstyp           | Beschreibung                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Schreibgeschützt<br/>  | Ruft ab, ob der Remotedesktopverbindung -Client (RDC) remoteApp-Funktionen unterstützt.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lesen/Schreiben<br/> | Ruft ab, ob der öffentliche Modus aktiviert ist.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lesen/Schreiben<br/> | Streamversion der RDP-Konfigurationsdatei.<br/>                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell ist als d012ae6d-c19a-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

