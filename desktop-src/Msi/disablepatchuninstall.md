---
description: Wenn diese Systemrichtlinie pro Computer auf 1 festgelegt ist, können Patches nicht von einem Benutzer oder Administrator vom Computer entfernt werden.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5531d5afd7fa98883a3e07dc7c47db625db9051fa223ea7cd6f70e4ceb5aee03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378568"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Wenn diese [Systemrichtlinie](system-policy.md) pro Computer auf 1 festgelegt ist, können Patches nicht von einem Benutzer oder Administrator vom Computer entfernt werden. Der Windows Installer kann weiterhin einen Patch entfernen, der nicht mehr auf ein Produkt anwendbar ist. Wenn diese Richtlinie nicht festgelegt ist, kann ein Benutzer nur dann einen Patch vom Computer entfernen, wenn dem Benutzer Berechtigungen zum Entfernen des Patches erteilt wurden. Dies kann davon abhängen, ob der Benutzer Administrator ist, ob [DisableMsi-](disablemsi.md) und [AlwaysInstallElevated-Richtlinieneinstellungen](alwaysinstallelevated.md) festgelegt sind und ob der Patch in einem pro Benutzer verwalteten, nicht verwalteten benutzerbezogenen oder computerbezogenen Kontext installiert wurde.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



