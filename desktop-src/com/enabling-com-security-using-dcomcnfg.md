---
title: Aktivieren der com-Sicherheit mithilfe von DCOMCNFG
description: "\"Dcomcnfg.exe\" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können."
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340422"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Aktivieren der com-Sicherheit mithilfe von DCOMCNFG

"Dcomcnfg.exe" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können. Mithilfe von Dcomcnfg.exe können Sie die Sicherheit entweder auf Computer-oder Prozessebene aktivieren. Sie können die Sicherheit für einen bestimmten Computer aktivieren, sodass, wenn ein Prozess weder Programm gesteuert noch durch Registrierungs Werte seine eigenen Sicherheitseinstellungen bereitstellt, die von Dcomcnfg.exe festgelegten Werte verwendet werden. Oder Sie können Dcomcnfg.exe verwenden, um die Sicherheit nur für eine bestimmte Anwendung zu aktivieren.

Wenn Sie die Sicherheit aktivieren, müssen Sie zwei Hauptaufgaben ausführen:

-   Legen Sie eine Authentifizierungs Ebene fest, die nicht "None" ist.
-   Legen Sie Berechtigungen fest, einschließlich Start-und Zugriffsberechtigungen.

Die Schritte, die zum Ausführen dieser Aufgaben ausgeführt werden, hängen davon ab, ob Sie die Sicherheit für den gesamten Computer oder nur für eine bestimmte Anwendung aktivieren. Sie können auch andere Werte für den Computer oder die Anwendung festlegen.

> [!Note]  
> Sie müssen ein Administrator sein, um Dcomcnfg.exe ausführen zu können.

 

Die folgenden Themen enthalten Schritt-für-Schritt-Anleitungen zum Festlegen der Sicherheit mit Dcomcnfg.exe:

-   [Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Festlegen der Processwide-Sicherheit mithilfe von DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> <dt>

[Ausschalten der Sicherheit](turning-off-security.md)
</dt> </dl>

 

 




