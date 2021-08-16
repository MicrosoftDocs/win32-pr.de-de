---
description: Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit. Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Autorisierungs-Manager-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784193"
---
# <a name="authorization-manager-model"></a>Autorisierungs-Manager-Modell

Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit. Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.

Autorisierungs-Manager-Anwendungen speichern Autorisierungsrichtlinien in Form von Autorisierungsspeichern, die in Active Directory- oder XML-Dateien gespeichert sind und Autorisierungsrichtlinien zur Laufzeit anwenden.

Anwendungen rufen dann eine Laufzeit-Zugriffsüberprüfungsmethode auf, die den Zugriff auf die Richtlinieninformationen im Autorisierungsspeicher überprüft.

Die Autorisierungsrichtlinie umfasst die folgenden Teile:

-   [Richtlinienspeicher, Anwendungen und Bereiche](policy-stores--applications--and-scopes.md)
-   [Benutzer und Gruppen](users-and-groups.md)
-   [Vorgänge und Aufgaben](operations-and-tasks.md)
-   [Rollen](roles.md)
-   [Geschäftsregeln](business-rules.md)
-   [Sammlungen](collections.md)

 

 



