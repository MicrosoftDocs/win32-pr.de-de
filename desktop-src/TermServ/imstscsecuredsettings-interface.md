---
title: Imstscsecuredsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind. | Imstscsecuredsettings-Schnittstelle
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355759"
---
# <a name="imstscsecuredsettings-interface"></a>Imstscsecuredsettings-Schnittstelle

Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind. Zu den Eigenschaften gehören diejenigen, die den Modus des Client Steuer Elements (Vollbildmodus oder Fenstermodus) und das Programm angeben, das bei der Verbindung mit dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) gestartet werden soll. Diese Methoden sind auch über die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle verfügbar.

## <a name="members"></a>Member

Die **imstscsecuredsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Imstscsecuredsettings** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imstscsecuredsettings** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                              | Zugriffstyp           | BESCHREIBUNG                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**FullScreen**](imstscsecuredsettings-fullscreen.md)<br/>     | Lesen/Schreiben<br/> | Der voll Bild Zustand des Client Steuer Elements.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Lesen/Schreiben<br/> | Das Programm, das auf dem Remote Server bei der Verbindung gestartet werden soll.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Lesen/Schreiben<br/> | Das Arbeitsverzeichnis des Start Programms.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den Methoden dieser Schnittstelle finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

