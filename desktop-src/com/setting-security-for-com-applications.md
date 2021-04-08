---
title: Festlegen der Sicherheit für COM-Anwendungen
description: Festlegen der Sicherheit für COM-Anwendungen
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857019"
---
# <a name="setting-security-for-com-applications"></a>Festlegen der Sicherheit für COM-Anwendungen

Es gibt mehrere Möglichkeiten, die Sicherheit für Ihre Anwendungen zu steuern. Sie können die Standard Sicherheitseinstellungen eines Computers ändern, die von allen Anwendungen auf dem Computer verwendet werden, die keine eigenen Sicherheitswerte bereitstellen. Sie können die Sicherheit für einen bestimmten Prozess entweder mithilfe von Dcomcnfg.exe oder durch Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen. Sie können Sicherheitseinstellungen auch Programm gesteuert auf der Schnittstellen Proxy Ebene steuern.

Die folgenden Themen enthalten Verfahren zum Festlegen der Sicherheit:

-   [Ändern der Sicherheits Standardwerte für einen Computer](modifying-the-security-defaults-for-a-computer.md)
-   [Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
-   [Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




