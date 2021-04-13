---
description: Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit. Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Authorization Manager-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350609"
---
# <a name="authorization-manager-model"></a>Authorization Manager-Modell

Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit. Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.

Autorisierungs-Manager-Anwendungen speichern Autorisierungsrichtlinien in Form von Autorisierungsspeichern, die in Active Directory- oder XML-Dateien gespeichert sind und Autorisierungsrichtlinien zur Laufzeit anwenden.

Anwendungen aufrufen dann eine Lauf Zeit Zugriffs Überprüfung-Methode, die den Zugriff auf die Richtlinien Informationen im Autorisierungs Speicher überprüft.

Die Autorisierungs Richtlinie umfasst die folgenden Teile:

-   [Richtlinien Speicher, Anwendungen und Bereiche](policy-stores--applications--and-scopes.md)
-   [Benutzer und Gruppen](users-and-groups.md)
-   [Vorgänge und Aufgaben](operations-and-tasks.md)
-   [Rollen](roles.md)
-   [Geschäftsregeln](business-rules.md)
-   [Sammlungen](collections.md)

 

 



