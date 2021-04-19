---
title: Festlegen Process-Wide Sicherheit
description: Es gibt mehrere Möglichkeiten, die Prozess weite Sicherheit festzulegen.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338625"
---
# <a name="setting-process-wide-security"></a>Festlegen Process-Wide Sicherheit

Es gibt mehrere Möglichkeiten, die Prozess weite Sicherheit festzulegen. Die erste Möglichkeit, das Dcomcnfg.exe Tool zu verwenden, ist die einfachste Methode, da Sie keine Programmierung erfordert. Das zweite Verfahren bietet dem Programmierer mehr Kontrolle und erfordert einen [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf. Eine andere Möglichkeit besteht darin, die Prozess weite Sicherheit in der Registrierung mithilfe des [AppID](appid-key.md) -Schlüssels festzulegen.

Weitere Informationen zu diesen Techniken finden Sie in den folgenden Themen:

-   [Festlegen der Process-Wide Sicherheit mithilfe von DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Festlegen der Process-Wide Sicherheit mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Festlegen der Process-Wide Sicherheit über die Registrierung](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




