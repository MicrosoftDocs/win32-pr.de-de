---
title: IMsRdpWorkspace2-Schnittstelle
description: Macht eine Methode verfügbar, die RemoteApp- und Desktopverbindung Anmeldeinformationen einer Verbindung zugeordnet.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125520"
---
# <a name="imsrdpworkspace2-interface"></a>IMsRdpWorkspace2-Schnittstelle

Macht eine Methode verfügbar, die RemoteApp- und Desktopverbindung Anmeldeinformationen einer Verbindung zugeordnet. Diese Schnittstelle wird vom Remotedesktopdienste Webzugriff-Steuerelement implementiert. Dieses Steuerelement ist ein Wrapper um den Remotedesktopverbindung-Client (MsTscAx.dll) und den RemoteApp- und Desktopverbindungs-Laufzeitproxy (Tswbprxy.exe).

## <a name="members"></a>Member

Die **IMsRdpWorkspace-Schnittstelle** erbt von [**IMsRdpWorkspace.**](imsrdpworkspace.md) **IMsRdpWorkspace2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMsRdpWorkspace-Schnittstelle** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Ordnet Benutzeranmeldeinformationen und Zertifikate einer Verbindungs-ID zu. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | \_IID-IMsRdpWorkspace2 ist als 145D0622-04CF-4FC3-A776-A82A9169CDF8 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

