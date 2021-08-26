---
title: Remotedesktopdienste WMI-Anbieter
description: Der Remotedesktopdienste-WMI-Anbieter bietet programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Remotedesktopdienste Configuration/Connections Microsoft Management Console-Snap-In (MMC) verfügbar gemacht werden.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste , WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4ed84dee9b2521c392b8b39ee1297121a85e1c4f8ad41f7d96d0d73042a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869600"
---
# <a name="remote-desktop-services-wmi-provider"></a>Remotedesktopdienste WMI-Anbieter

Der Remotedesktopdienste-WMI-Anbieter bietet programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Remotedesktopdienste Configuration/Connections Microsoft Management Console-Snap-In (MMC) verfügbar gemacht werden.

Die Anbieter-DLL wird vom Windows Management-Prozess (Winmgmt.exe) geladen, wenn ein Client eine Anforderung an den Server sendet. Die Verwaltung ist mithilfe der Anbietermethoden möglich. Der Anbieter wird sowohl als Instanz als auch als Methodenanbieter registriert.

Der Remotedesktopdienste WMI-Anbieter wurde als dynamischer Anbieter implementiert, der von der [**Win32 \_ Service-Basisklasse**](/windows/desktop/CIMWin32Prov/win32-service) abgeleitet wurde und alle eigenschaften und Methoden erbt, sowie eine in Bearbeitung enthaltene Dynamic Link Library.

Weitere Informationen finden Sie in der Remotedesktopdienste [WMI-Anbieterreferenz.](terminal-services-wmi-provider-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktopdienste WMI-Anbieterreferenz](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 