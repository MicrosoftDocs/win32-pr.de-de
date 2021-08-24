---
description: Die ACTION-Eigenschaft kann auf die folgenden Werte festgelegt werden.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145993"
---
# <a name="action-property"></a>ACTION-Eigenschaft

Die **ACTION-Eigenschaft** kann auf die folgenden Werte festgelegt werden.

## <a name="value"></a>Wert



| Wert                                                                                                                                            | Bedeutung                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**Installieren**</dt> </dl>       | [INSTALL-Aktion](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**Werben**</dt> </dl> | [AKTION "ANKNEN"](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**Admin**</dt> </dl>             | [ADMIN-Aktion](admin-action.md)<br/>         |



 

Die **ACTION-Eigenschaft** bestimmt, welche Aktion ausgeführt werden soll, wenn ein NULL-Aktionsname für [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) oder die [**DoAction-Methode angegeben wird.**](session-doaction.md) Wenn kein Wert für die **ACTION-Eigenschaft definiert** ist, ruft das Installationsprogramm die [INSTALL-Aktion auf.](install-action.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




