---
description: Wenn diese pro-Computer-System Richtlinie auf 1 festgelegt ist, können Patches von einem Benutzer oder Administrator nicht vom Computer entfernt werden.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: Disablepatchuninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863043"
---
# <a name="disablepatchuninstall"></a>Disablepatchuninstall

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf 1 festgelegt ist, können Patches von einem Benutzer oder Administrator nicht vom Computer entfernt werden. Der Windows Installer kann weiterhin einen Patch entfernen, der für ein Produkt nicht mehr anwendbar ist. Wenn diese Richtlinie nicht festgelegt ist, kann ein Benutzer einen Patch nur dann vom Computer entfernen, wenn dem Benutzerberechtigungen zum Entfernen des Patches erteilt wurden. Dies kann davon abhängen, ob der Benutzer ein Administrator ist, ob die Richtlinien Einstellungen [DisableMSI](disablemsi.md) und [alwaysinstallerhöhten](alwaysinstallelevated.md) festgelegt sind und ob der Patch in einem pro Benutzer verwalteten, nicht verwalteten oder benutzerspezifischen Kontext installiert wurde.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



