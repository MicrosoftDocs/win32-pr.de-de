---
description: Mithilfe dieser System Richtlinie können Sie angeben, dass der Windows Installer während einer verwalteten Installation mithilfe erweiterter Berechtigungen Alle öffentlichen Eigenschaften an die Serverseite übergibt.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: Enableusercontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130685"
---
# <a name="enableusercontrol"></a>Enableusercontrol

Im Fall einer verwalteten Installation muss der Paket Ersteller möglicherweise einschränken, welche öffentlichen Eigenschaften an die Serverseite übermittelt werden, und er kann von einem Benutzer geändert werden, der kein Systemadministrator ist. Einige Einschränkungen sind im allgemeinen erforderlich, um eine sichere Umgebung zu verwalten, wenn die Installation erfordert, dass das Installationsprogramm erweiterte Berechtigungen verwendet.

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, kann das Installationsprogramm während einer verwalteten Installation mit erweiterten Berechtigungen alle [öffentlichen Eigenschaften](public-properties.md) an die Serverseite übergeben. Das Festlegen dieser Richtlinie hat dieselbe Auswirkung wie das Festlegen der **enableusercontrol** -Eigenschaft. Wenn Sie diese Richtlinie festlegen, können alle öffentlichen Eigenschaften an den Dienst übermittelt werden und können von nicht Administratoren geändert werden. Diese Richtlinie ist standardmäßig nicht aktiviert. nur eingeschränkte öffentliche Eigenschaften werden an die Serverseite übermittelt und können von einem nicht Administrator geändert werden. Alle anderen öffentlichen Eigenschaften werden ignoriert.

Wenn das Betriebssystem Windows 2000 ist, ist der Benutzer kein Systemadministrator, und die Anwendung bzw. das Produkt wird mit erhöhten Rechten installiert. ein Benutzer, der kein Systemadministrator ist, kann nur eine genehmigte Liste von eingeschränkten öffentlichen Eigenschaften außer Kraft setzen. Weitere Informationen finden Sie unter [Eingeschränkte öffentliche Eigenschaften](restricted-public-properties.md).

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



