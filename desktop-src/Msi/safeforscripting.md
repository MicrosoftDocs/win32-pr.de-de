---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , werden Benutzer vom Installationsprogramm nicht aufgefordert, wenn Skripts in einer Webseite die Automatisierungsschnittstelle des Installers verwenden.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: Safeforscripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354591"
---
# <a name="safeforscripting"></a>Safeforscripting

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, werden Benutzer vom Installationsprogramm nicht aufgefordert, wenn Skripts innerhalb einer Webseite die [Automatisierungsschnittstelle](automation-interface.md)des Installers verwenden.

Vor dem Festlegen dieser Richtlinie sollten Sie in Erwägung gezogen werden, ob die Benutzer Aufforderung eine entsprechende Sicherheitsstufe für Ihre Benutzer bereitstellt. Wenn diese Richtlinie nicht festgelegt ist und ein von einem Internet Browser gehosteter Skript versucht, eine Anwendung zu installieren, warnt das System den Benutzer und fordert Sie auf, die Installation zu akzeptieren oder abzulehnen. Durch das Festlegen von safeforscripting wird diese Warnung unterdrückt, und die Installation von Anwendungen auf dem System kann ohne das Wissen des Benutzers zugelassen werden. Diese Richtlinie kann für ein Unternehmen nützlich sein, das webbasierte Tools zum Verteilen von Programmen verwendet.

Weitere Informationen finden Sie unter [Richtlinien zum Erstellen sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und [Herunterladen einer-Installation aus dem Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



