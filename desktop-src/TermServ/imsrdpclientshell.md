---
title: Imsrdpclientshell-Schnittstelle
description: Remotedesktopverbindung (RDC)-Client Einstellungen, die verwendet werden, um den Client über Remotedesktop Webzugriff (RD Webzugriff) oder andere Webportale zu starten.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477757"
---
# <a name="imsrdpclientshell-interface"></a>Imsrdpclientshell-Schnittstelle

Remotedesktopverbindung (RDC)-Client Einstellungen, die verwendet werden, um den Client über Remotedesktop Webzugriff (RD Webzugriff) oder andere Webportale zu starten.

## <a name="members"></a>Member

Die **imsrdpclientshell** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Imsrdpclientshell** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **imsrdpclientshell** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**Getrdpproperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Ruft eine einzelne RDP-Eigenschaft ab.<br/>                  |
| [**Starten**](imsrdpclientshell-launch.md)                 | Starten von Remote Dateiinhalt über das Webportal.<br/> |
| [**""-Eigenschaft ""**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Legt eine einzelne RDP-Eigenschaft fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **imsrdpclientshell** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Isremoteprogramclientinstalliert**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Schreibgeschützt<br/>  | Ruft ab, ob der Remotedesktopverbindung-Client (RDC) die RemoteApp-Funktionalität unterstützt.<br/> |
| [**Publicmode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lesen/Schreiben<br/> | Ruft ab, ob der öffentliche Modus aktiviert ist.<br/>                                                      |
| [**Rdpfilecontents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lesen/Schreiben<br/> | Streamversion der RDP-Konfigurationsdatei.<br/>                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

