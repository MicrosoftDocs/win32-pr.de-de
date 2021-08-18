---
description: Erläutert die Teile des Zugriffssteuerungsmodells.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Teile des Access Control Modells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785670"
---
# <a name="parts-of-the-access-control-model"></a>Teile des Access Control Modells

Es gibt zwei grundlegende Teile des Zugriffssteuerungsmodells:

-   [Zugriffstoken,](access-tokens.md)die Informationen zu einem angemeldeten Benutzer enthalten
-   [Sicherheitsdeskriptoren,](security-descriptors.md)die die Sicherheitsinformationen enthalten, die ein sicherungsfähiges [Objekt schützen](securable-objects.md)

Wenn sich ein Benutzer anmeldet, [*authentifiziert*](/windows/desktop/SecGloss/a-gly) das System den Kontonamen und das Kennwort des Benutzers. Wenn die Anmeldung erfolgreich ist, erstellt das System ein Zugriffstoken. Jeder [*Prozess,*](/windows/desktop/SecGloss/p-gly) der im Namen dieses Benutzers ausgeführt wird, enthält eine Kopie dieses Zugriffstokens. Das Zugriffstoken enthält [Sicherheits-IDs,](security-identifiers.md) die das Konto des Benutzers und alle Gruppenkonten identifizieren, zu denen der Benutzer gehört. Das Token enthält auch eine Liste der Berechtigungen [des](privileges.md) Benutzers oder der Gruppen des Benutzers. Das System verwendet dieses Token, um den zugeordneten Benutzer zu identifizieren, wenn ein Prozess versucht, auf ein sicherungsfähiges Objekt zu zugreifen oder eine Systemverwaltungsaufgabe auszuführen, die Berechtigungen erfordert.

Wenn ein sicherungsfähiges Objekt erstellt wird, [](/windows/desktop/SecGloss/s-gly) weist das System ihm einen Sicherheitsdeskriptor zu, der sicherheitsinformationen enthält, die vom Ersteller angegeben wurden, oder Standardsicherheitsinformationen, wenn keine angegeben sind. Anwendungen können Funktionen zum Abrufen und Festlegen der Sicherheitsinformationen für ein vorhandenes Objekt verwenden.

Ein Sicherheitsdeskriptor identifiziert den Besitzer des Objekts und kann auch die folgenden [Zugriffssteuerungslisten enthalten:](access-control-lists.md)

-   Eine [*DACL (Discretionary Access Control List),*](/windows/desktop/SecGloss/d-gly) die die Benutzer und Gruppen identifiziert, denen der Zugriff auf das Objekt erlaubt oder verweigert wurde.
-   Eine [*SACL (System Access Control List),*](/windows/desktop/SecGloss/s-gly) die steuert, wie das System [versucht,](audit-generation.md) auf das Objekt zu zugreifen.

Eine Zugriffssteuerungsliste enthält eine Liste von [Zugriffssteuerungseinträgen](access-control-entries.md) (ACEs). Jeder ACE gibt einen Satz von Zugriffsrechten [an](access-rights-and-access-masks.md) und enthält eine SID, die einen Vertrauenshänder identifiziert, für den die Rechte zugelassen, verweigert oder überwacht werden. [](trustees.md) Ein Vertrauensinhaber kann ein Benutzerkonto, ein Gruppenkonto oder eine [*Anmeldesitzung sein.*](/windows/desktop/SecGloss/l-gly)

Verwenden Sie Funktionen, um den Inhalt von Sicherheitsbeschreibungen, SIDs und ACLs zu bearbeiten, anstatt direkt darauf zu zugreifen. Dadurch wird sichergestellt, dass diese Strukturen syntaktisch genau bleiben, und verhindert, dass zukünftige Verbesserungen des Sicherheitssystems vorhandenen Code unterbricht.

Die folgenden Themen enthalten Informationen zu Teilen des Zugriffssteuerungsmodells:

-   [Zugriffstoken](access-tokens.md)
-   [Sicherheitsbeschreibungen](security-descriptors.md)
-   [Access Control Listen](access-control-lists.md)
-   [Access Control Einträge](access-control-entries.md)
-   [Zugriffsrechte und Zugriffsmasken](access-rights-and-access-masks.md)
-   [Funktionsweise von AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Zentralisierte Autorisierungsrichtlinie](centralized-authorization-policy.md)
-   [Sicherheits-IDs](security-identifiers.md)

 

 
