---
title: Benutzer wird gestartet
description: Benutzer wird gestartet
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858491"
---
# <a name="launching-user"></a>Benutzer wird gestartet

Dies ist die Standardeinstellung für die Anwendungs Identität. Wenn der Start Benutzer für die Identität der Anwendung ausgewählt wird, erhält jedes Client Konto eine neue Instanz des Servers, und jeder Server erhält seine eigene [Fenster Station](/windows/desktop/winstation/window-stations). Aufgrund der separaten Server Instanzen ist das Starten des Benutzers die Sicherheitsschutz-Identitäts Einstellung auf höchster Ebene. Es gibt jedoch endliche Grenzwerte für den Ressourcenverbrauch. Außerdem wird jede GUI, die der Server anzeigt, vom Client nicht angezeigt.

Wenn die Anwendung über die Identität des Start Benutzers verfügt, wird Sie mit einem Identitätswechsel Token ausgeführt. Weitere Informationen zu Identitäts [Wechsel-und](cloaking.md)Zugriffs Token finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und-Verschleierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Identität](application-identity.md)
</dt> <dt>

[Interaktiver Benutzer](interactive-user.md)
</dt> <dt>

[Dienst Identität](service-identity.md)
</dt> <dt>

[Angegebener Benutzer](specified-user.md)
</dt> </dl>

 

 