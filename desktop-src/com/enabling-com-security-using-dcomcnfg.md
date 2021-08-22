---
title: Aktivieren der COM-Sicherheit mithilfe von DCOMCNFG
description: "\"Dcomcnfg.exe\" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können."
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6161cf7418e7eab705203df51710e789ad2ef7d6843051dd35399fb8388f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678690"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Aktivieren der COM-Sicherheit mithilfe von DCOMCNFG

"Dcomcnfg.exe" verfügt über eine Benutzeroberfläche, über die Sie bestimmte Einstellungen in der Registrierung ändern können. Mit Dcomcnfg.exe können Sie die Sicherheit entweder computerweit oder prozessweit aktivieren. Sie können die Sicherheit für einen bestimmten Computer aktivieren, sodass die von einem Prozess festgelegten Werte verwendet werden, wenn er keine eigenen Sicherheitseinstellungen entweder programmgesteuert oder über Registrierungswerte Dcomcnfg.exe. Oder Sie können Dcomcnfg.exe verwenden, um die Sicherheit nur für eine bestimmte Anwendung zu aktivieren.

Beim Aktivieren der Sicherheit müssen zwei Hauptaufgaben erfüllt werden:

-   Legen Sie eine Authentifizierungsebene fest, die nicht None ist.
-   Legen Sie Berechtigungen fest, einschließlich Start- und Zugriffsberechtigungen.

Welche Schritte zum Ausführen dieser Aufgaben erforderlich sind, hängt davon ab, ob Sie die Sicherheit für den gesamten Computer oder nur für eine bestimmte Anwendung aktivieren. Möglicherweise möchten Sie auch andere Werte für den Computer oder die Anwendung festlegen.

> [!Note]  
> Sie müssen Administrator sein, um die Dcomcnfg.exe.

 

Die folgenden Themen enthalten schritt-für-Schritt-Verfahren zum Festlegen der Sicherheit mit Dcomcnfg.exe:

-   [Festlegen System-Wide-Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Festlegen der prozessweiten Sicherheit mithilfe von DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> <dt>

[Deaktivieren der Sicherheit](turning-off-security.md)
</dt> </dl>

 

 




