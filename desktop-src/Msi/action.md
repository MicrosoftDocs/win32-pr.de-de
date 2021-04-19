---
description: Die Action-Eigenschaft kann auf die folgenden Werte festgelegt werden.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Action-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360895"
---
# <a name="action-property"></a>Action-Eigenschaft

Die **Action** -Eigenschaft kann auf die folgenden Werte festgelegt werden.

## <a name="value"></a>Wert



| Wert                                                                                                                                            | Bedeutung                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**Installieren**</dt> </dl>       | [Installations Aktion](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**Benen**</dt> </dl> | [Aktion ankündigen](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**Administrator**</dt> </dl>             | [Administrator Aktion](admin-action.md)<br/>         |



 

Die **Action** -Eigenschaft bestimmt, welche Aktion ausgeführt werden soll, wenn ein NULL-Aktionsname für [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) oder die [**doaction-Methode**](session-doaction.md)angegeben wird. Wenn für die **Action** -Eigenschaft kein Wert definiert ist, ruft das Installationsprogramm die [Installations Aktion](install-action.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




