---
description: Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: Enableadminout-Remote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215128"
---
# <a name="enableadmintsremote"></a>Enableadminout-Remote

Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr. Ein Administrator kann eine Installation über die Konsolen Sitzung eines Terminal Servers ausführen. Ein Administrator kann auch eine Installation aus einer Client Sitzung des Terminal Servers ausführen.

Weitere Informationen finden Sie unter [Terminal Dienste](/windows/desktop/TermServ/terminal-services-portal) im Microsoft Windows Software Development Kit (SDK).

* * Betriebssysteme vor Windows Server 2008 und Windows Vista: * *

Durch Festlegen dieser computerspezifischen [System Richtlinie](system-policy.md) können Administratoren Installationen aus einer Client Sitzung des Terminal Servers ausführen. Wenn diese Richtlinie nicht festgelegt ist, können Administratoren nur Installationen aus der Konsolen Sitzung ausführen. Nicht Administratoren können niemals Installationen aus einer Client Sitzung ausführen. Der Standardwert für diese Richtlinie ermöglicht es nur Administratoren, Installationen über die Konsolen Sitzung auszuführen. Administratoren können immer [administrative Installationen](administrative-installation.md) über eine Client Sitzung des Terminal Servers oder über die Konsolen Sitzung ausführen, unabhängig davon, ob diese Richtlinie festgelegt ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden [Sie unter Verwenden von Windows Installer mit einem Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
