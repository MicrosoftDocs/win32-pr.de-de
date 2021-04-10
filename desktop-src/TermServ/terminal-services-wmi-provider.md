---
title: WMI-Anbieter Remotedesktopdienste
description: Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039153"
---
# <a name="remote-desktop-services-wmi-provider"></a>WMI-Anbieter Remotedesktopdienste

Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.

Die Anbieter-DLL wird vom Windows-Verwaltungsprozess (Winmgmt.exe) geladen, wenn ein Client eine Anforderung an den Server sendet. Die Verwaltung ist möglich, indem die Anbieter Methoden verwendet werden. Der Anbieter ist sowohl als Instanz als auch als Methoden Anbieter registriert.

Der Remotedesktopdienste WMI-Anbieter wurde als dynamischer Anbieter implementiert, der von der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Basisklasse abgeleitet wurde, und erbt dabei alle seine Eigenschaften und Methoden sowie eine Prozess interne Dynamic Link Library.

Weitere Informationen finden Sie in der [Remotedesktopdienste WMI-Anbieter Referenz](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Anbieter Referenz Remotedesktopdienste](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 