---
title: IMsRdpWorkspace-Schnittstelle
description: Macht Methoden verfügbar, die RemoteApp- und Desktopverbindung Anmeldeinformationen und Verbindungen verwalten.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- IMsRdpWorkspace-Schnittstelle Remotedesktopdienste
- IMsRdpWorkspace-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1489690632b0ef1bf05a529d84ed5c96afb6c442c82744f964c9a89e9286299d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125530"
---
# <a name="imsrdpworkspace-interface"></a>IMsRdpWorkspace-Schnittstelle

Macht Methoden verfügbar, die RemoteApp- und Desktopverbindung Anmeldeinformationen und Verbindungen verwalten. Diese Schnittstelle wird vom Remotedesktopdienste Webzugriff-Steuerelement implementiert. Dieses Steuerelement ist ein Wrapper um den Remotedesktopverbindung-Client (MsTscAx.dll) und den RemoteApp- und Desktopverbindungs-Laufzeitproxy (Tswbprxy.exe).

## <a name="members"></a>Member

Die **IMsRdpWorkspace-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpWorkspace** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMsRdpWorkspace-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Löscht die Benutzeranmeldeinformationen, die der angegebenen Verbindungs-ID zugeordnet sind.<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Trennt alle vorhandenen Verbindungen, die der angegebenen Verbindungs-ID zugeordnet sind, und löscht die entsprechenden Benutzeranmeldeinformationen aus dem Anmeldeinformationsspeicher.<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Bestimmt, ob Benutzeranmeldeinformationen für die angegebene Verbindungs-ID vorhanden sind.<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Bestimmt, ob einmaliges Anmelden (Single Sign On, SSO) für RemoteApp- und Desktopverbindung aktiviert ist.<br/>                                                                   |
| [**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Markiert die Authentifizierung von Benutzeranmeldeinformationen für die Verbindungs-ID und zeigt anschließend die Verbindungsbenachrichtigung im Taskleistenbenachrichtigungsbereich an. <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Ordnet Benutzeranmeldeinformationen und Zertifikate einer Verbindungs-ID zu.<br/>                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace ist als 145D0621-04CF-4FC2-A766-A81A9069CDF8 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

