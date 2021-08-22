---
title: IMsRdpClientShell2-Schnittstelle
description: Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder über andere Webportale starten.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e9a63e631ca88575f4b632def5e47b29b68da414d48af95d42e757dcb2da6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138653"
---
# <a name="imsrdpclientshell2-interface"></a>IMsRdpClientShell2-Schnittstelle

Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder über andere Webportale starten.

Diese Schnittstelle wird von der Remotedesktopdienste Webzugriff Control implementiert. Dabei handelt es sich um einen Wrapper um den Remotedesktopverbindung-Client (MsTscAx.dll) und den Laufzeitproxy für RemoteApp- und Desktopverbindungen (Tswbprxy.exe).

## <a name="members"></a>Member

Die **IMsRdpClientShell2-Schnittstelle** erbt von **IMsRdpClientShell.** **IMsRdpClientShell2** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientShell2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                               | Zugriffstyp          | Beschreibung                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Schreibgeschützt<br/> | Ruft einen Zeiger auf die [**IMsRdpWorkspace-Schnittstelle**](imsrdpworkspace.md) ab, die zum Verwalten RemoteApp- und Desktopverbindung Anmeldeinformationen und Verbindungen verwendet wird.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer URL-Sicherheitszone befindet.<br/>                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





