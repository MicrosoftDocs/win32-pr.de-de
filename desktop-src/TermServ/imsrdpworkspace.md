---
title: Imsrdpworkspace-Schnittstelle
description: Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- Imsrdpworkspace-Schnittstelle Remotedesktopdienste
- Imsrdpworkspace-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949500"
---
# <a name="imsrdpworkspace-interface"></a>Imsrdpworkspace-Schnittstelle

Macht Methoden verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwalten. Diese Schnittstelle wird von der Remotedesktopdienste Webzugriff-Steuerelement implementiert. Dieses Steuerelement ist ein Wrapper um den Remotedesktopverbindung Client (MsTscAx.dll) und den Lauf Zeit Proxy für RemoteApp-und Desktop Verbindungen (Tswbprxy.exe).

## <a name="members"></a>Member

Die **imsrdpworkspace** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Imsrdpworkspace** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imsrdpworkspace** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clearworkspacecredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Löscht die Benutzer Anmelde Informationen, die der angegebenen Verbindungs-ID zugeordnet sind.<br/>                                                                                  |
| [**Disconnectworkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Trennt alle vorhandenen Verbindungen, die mit der angegebenen Verbindungs-ID verknüpft sind, und löscht die entsprechenden Benutzer Anmelde Informationen aus dem Anmelde Informationsspeicher.<br/> |
| [**Isworkspacecredentialspezifiziert**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Bestimmt, ob Benutzer Anmelde Informationen für die angegebene Verbindungs-ID vorhanden sind.<br/>                                                                                 |
| [**Isworkspacessoaktivierte**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Bestimmt, ob einmaliges Anmelden (Single Sign on, SSO) für RemoteApp-und Desktopverbindung aktiviert ist.<br/>                                                                   |
| [**Onauthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Markiert die Authentifizierung der Benutzer Anmelde Informationen für die Verbindungs-ID und zeigt anschließend die Verbindungs Benachrichtigung im Benachrichtigungsbereich der Taskleiste an. <br/>     |
| [**Startworkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Ordnet Benutzer Anmelde Informationen und Zertifikate einer Verbindungs-ID zu.<br/>                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpworkspace ist als 145d0621-04cf-4fc2-a766-a81a9069cdf8 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

