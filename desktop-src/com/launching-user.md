---
title: Starten des Benutzers
description: Starten des Benutzers
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e04163d5229942abff55339d53ba37ec0f8bdc6e9ac60b0893f1d243b22643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736536"
---
# <a name="launching-user"></a>Starten des Benutzers

Dies ist die Standardeinstellung für die Anwendungsidentität. Wenn der startde Benutzer für die Identität der Anwendung ausgewählt wird, erhält jedes Clientkonto eine neue Instanz des Servers, und jeder Server erhält seine eigene [Fensterstation.](/windows/desktop/winstation/window-stations) Aufgrund der separaten Serverinstanzen ist das Starten des Benutzers die Höchste Ebene der Sicherheitsschutz-Identitätseinstellung. Es gibt jedoch begrenzte Grenzwerte für den Ressourcenverbrauch. Außerdem wird jede gui, die der Server anzeigt, vom Client nicht angezeigt.

Wenn die Anwendung über die Identität des startden Benutzers verfügt, wird sie mit einem Identitätswechseltoken ausgeführt. Weitere Informationen zu Identitätswechsel und Zugriffstoken finden Sie unter [Identitätswechselebenen](impersonation-levels.md) und [Cloaking](cloaking.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsidentität](application-identity.md)
</dt> <dt>

[Interaktiver Benutzer](interactive-user.md)
</dt> <dt>

[Dienstidentität](service-identity.md)
</dt> <dt>

[Angegebener Benutzer](specified-user.md)
</dt> </dl>

 

 