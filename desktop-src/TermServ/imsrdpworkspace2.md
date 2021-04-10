---
title: IMsRdpWorkspace2-Schnittstelle
description: Macht eine Methode verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen mit einer Verbindung verknüpft.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040535"
---
# <a name="imsrdpworkspace2-interface"></a>IMsRdpWorkspace2-Schnittstelle

Macht eine Methode verfügbar, die RemoteApp-und Desktopverbindung Anmelde Informationen mit einer Verbindung verknüpft. Diese Schnittstelle wird von der Remotedesktopdienste Webzugriff-Steuerelement implementiert. Dieses Steuerelement ist ein Wrapper um den Remotedesktopverbindung Client (MsTscAx.dll) und den Lauf Zeit Proxy für RemoteApp-und Desktop Verbindungen (Tswbprxy.exe).

## <a name="members"></a>Member

Die **imsrdpworkspace** -Schnittstelle erbt von [**imsrdpworkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imsrdpworkspace** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Startworkspaceex**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Ordnet Benutzer Anmelde Informationen und Zertifikate einer Verbindungs-ID zu. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 ist als 145d0622-04cf-4FC3-a776-a82a9169cdf8 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**Imsrdpworkspace**](imsrdpworkspace.md)
</dt> </dl>

 

