---
description: Wenn diese Systemrichtlinie pro Computer auf &\# 0034;1&\# 0034; festgelegt ist, fordert das Installationsprogramm Benutzer nicht auf, wenn Skripts innerhalb einer Webseite die Automatisierungsschnittstelle des Installationsprogramms verwenden.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9a78bded284a687994075fdda1276122df2ab68716c4aaf759b4f5750aeb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990150"
---
# <a name="safeforscripting"></a>SafeForScripting

Wenn diese [Systemrichtlinie](system-policy.md) pro Computer auf "1" festgelegt ist, werden Benutzer vom Installationsprogramm nicht aufgefordert, wenn Skripts auf einer Webseite die [Automatisierungsschnittstelle](automation-interface.md)des Installationsprogramms verwenden.

Bevor Sie diese Richtlinie festlegen, sollten Sie berücksichtigen, ob das Warten auf die Benutzereingabeaufforderung ein angemessenes Maß an Sicherheit für Ihre Benutzer bietet. Wenn diese Richtlinie nicht festgelegt ist und ein von einem Internetbrowser gehostetes Skript versucht, eine Anwendung zu installieren, warnt das System den Benutzer und fordert diesen auf, die Installation zu akzeptieren oder abzulehnen. Durch das Festlegen von SafeForScripting wird diese Warnung unterdrückt, und es kann die Installation von Anwendungen auf dem System ohne das Wissen des Benutzers zugelassen werden. Diese Richtlinie kann für ein Unternehmen nützlich sein, das webbasierte Tools zum Verteilen von Programmen verwendet.

Weitere Informationen finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und digitaler [Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und Herunterladen einer Installation aus dem [Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Microsoft \_** Windows Installer für \\ **lokale Computersoftwarerichtlinien** \\  \\  \\  \\ 

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



