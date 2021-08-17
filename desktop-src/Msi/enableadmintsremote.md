---
description: Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a644e6f0cb9200fd8a130a2cdb293e7658e3354b817f7378571fae0ab3b4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637104"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

Ab Windows Server 2008 und Windows Vista hat diese Richtlinie keine Auswirkungen mehr. Ein Administrator kann eine Installation über die Konsolensitzung eines Terminalservers ausführen. Ein Administrator kann auch eine Installation über eine Clientsitzung des Terminalservers ausführen.

Weitere Informationen finden Sie unter [Terminaldienste](/windows/desktop/TermServ/terminal-services-portal) im Microsoft Windows Software Development Kit (SDK).

**Betriebssysteme vor Windows Server 2008 und Windows Vista: **

Durch Festlegen dieser [Systemrichtlinie](system-policy.md) pro Computer können Administratoren Installationen über eine Clientsitzung des Terminalservers ausführen. Wenn diese Richtlinie nicht festgelegt ist, können Administratoren installationen nur über die Konsolensitzung ausführen. Nicht administrative Benutzer können niemals Installationen aus einer Clientsitzung ausführen. Der Standardwert für diese Richtlinie ermöglicht nur Administratoren das Ausführen von Installationen über die Konsolensitzung. Administratoren können [Verwaltungsinstallationen](administrative-installation.md) immer über eine Clientsitzung des Terminalservers oder über die Konsolensitzung durchführen, unabhängig davon, ob diese Richtlinie festgelegt ist.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie auch unter [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
