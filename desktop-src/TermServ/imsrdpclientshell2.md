---
title: IMsRdpClientShell2-Schnittstelle
description: Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder andere Webportale starten.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell2-Schnittstelle Remotedesktopdienste
- IMsRdpClientShell2 Interface Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740552"
---
# <a name="imsrdpclientshell2-interface"></a>IMsRdpClientShell2-Schnittstelle

Macht Eigenschaften verfügbar, die den Remotedesktopverbindung Client über Remotedesktop Webzugriff (RD-Webzugriff) oder andere Webportale starten.

Diese Schnittstelle wird durch das Remotedesktopdienste Webzugriff-Steuerelement implementiert. Hierbei handelt es sich um einen Wrapper um den Remotedesktopverbindung Client (MsTscAx.dll) und den Lauf Zeit Proxy für RemoteApp-und Desktop Verbindungen (Tswbprxy.exe).

## <a name="members"></a>Member

Die **IMsRdpClientShell2** -Schnittstelle erbt von **imsrdpclientshell**. **IMsRdpClientShell2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientShell2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                               | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msrdpworkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Schreibgeschützt<br/> | Ruft einen Zeiger auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.<br/> |
| [**Securedsettingsenabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Schreibgeschützt<br/> | Ruft einen Wert ab, der angibt, ob sich die aktuelle Webseite in einer vertrauenswürdigen Internet Explorer-URL-Sicherheitszone befindet.<br/>                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpworkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





