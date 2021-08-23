---
description: Diese Computerspezifische Systemrichtlinie kann verwendet werden, um anzugeben, dass der Windows Installer während einer verwalteten Installation mit erhöhten Rechten alle öffentlichen Eigenschaften an die Serverseite überweist.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d8c56b1ea4d161030b252141e1930bd8298cea98b52b09511175d132e6a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637006"
---
# <a name="enableusercontrol"></a>EnableUserControl

Bei einer verwalteten Installation muss der Paketautor möglicherweise einschränken, welche öffentlichen Eigenschaften an die Serverseite übergeben werden und von einem Benutzer geändert werden können, der kein Systemadministrator ist. Einige Einschränkungen sind häufig erforderlich, um eine sichere Umgebung zu gewährleisten, wenn das Installationsprogramm erhöhte Rechte verwenden muss.

Wenn diese computerspezifische [Systemrichtlinie](system-policy.md) auf "1" festgelegt ist, [](public-properties.md) kann das Installationsprogramm alle öffentlichen Eigenschaften während einer verwalteten Installation mit erhöhten Rechten an die Serverseite übergeben. Das Festlegen dieser Richtlinie hat die gleiche Auswirkung wie das Festlegen der **EnableUserControl-Eigenschaft.** Durch festlegen dieser Richtlinie können alle öffentlichen Eigenschaften an den Dienst übergeben und von nichtadministrativen Benutzern geändert werden. Standardmäßig ist diese Richtlinie nicht aktiviert. nur eingeschränkte öffentliche Eigenschaften werden an die Serverseite übergeben und können von einem nichtadministrativen Benutzer geändert werden. Alle anderen öffentlichen Eigenschaften werden ignoriert.

Wenn das Betriebssystem Windows 2000 ist, der Benutzer kein Systemadministrator ist und die Anwendung oder das Produkt mit erhöhten Rechten installiert wird, kann ein Benutzer, der kein Systemadministrator ist, nur eine genehmigte Liste eingeschränkter öffentlicher Eigenschaften überschreiben. Weitere Informationen finden Sie unter [Eingeschränkte öffentliche Eigenschaften.](restricted-public-properties.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



