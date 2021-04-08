---
description: Erläutert die Teile des Zugriffs Steuerungs Modells.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Teile des Access Control Modells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3aa6d3547d486c33f4b31cdb5d5de24c7d27cec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864376"
---
# <a name="parts-of-the-access-control-model"></a>Teile des Access Control Modells

Es gibt zwei grundlegende Teile des Zugriffs Steuerungs Modells:

-   [Zugriffs Token](access-tokens.md), die Informationen zu einem angemeldeten Benutzer enthalten
-   [Sicherheits Deskriptoren](security-descriptors.md), die die Sicherheitsinformationen enthalten, die ein Sicherungs [fähiges Objekt](securable-objects.md) schützen

Wenn sich ein Benutzer anmeldet, [*authentifiziert*](/windows/desktop/SecGloss/a-gly) das System den Kontonamen und das Kennwort des Benutzers. Wenn die Anmeldung erfolgreich ist, erstellt das System ein Zugriffs Token. Jeder [*Prozess*](/windows/desktop/SecGloss/p-gly) , der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens. Das Zugriffs Token enthält [Sicherheits](security-identifiers.md) -IDs, die das Benutzerkonto und alle Gruppenkonten identifizieren, zu denen der Benutzer gehört. Das Token enthält außerdem eine Liste der [Berechtigungen](privileges.md) , die der Benutzer oder die Benutzergruppen innehat. Das System verwendet dieses Token, um den zugeordneten Benutzer zu identifizieren, wenn ein Prozess versucht, auf ein Sicherungs fähiges Objekt zuzugreifen oder eine System Verwaltungsaufgabe auszuführen, für die Berechtigungen erforderlich sind.

Wenn ein Sicherungs fähiges Objekt erstellt wird, weist das System ihm eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) zu, die vom Ersteller angegebene Sicherheitsinformationen enthält, oder Standard Sicherheitsinformationen, wenn keine Angabe erfolgt. Anwendungen können Funktionen verwenden, um die Sicherheitsinformationen für ein vorhandenes Objekt abzurufen und festzulegen.

Eine Sicherheits Beschreibung identifiziert den Besitzer des Objekts und kann auch die folgenden [Zugriffs Steuerungs Listen](access-control-lists.md)enthalten:

-   Eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL), die die Benutzer und Gruppen identifiziert, denen der Zugriff auf das Objekt gewährt oder verweigert wird.
-   Eine SACL ( [*System Access Control List*](/windows/desktop/SecGloss/s-gly) ), mit der gesteuert wird, wie die System Überwachungen [versuchen,](audit-generation.md) auf das Objekt zuzugreifen.

Eine ACL enthält eine Liste von [Zugriffs Steuerungs Einträgen](access-control-entries.md) (ACEs). Jeder ACE gibt eine Gruppe von [Zugriffsrechten](access-rights-and-access-masks.md) an und enthält eine SID, die einen Vertrauens nehmer identifiziert [, für den](trustees.md) die Rechte gewährt, verweigert oder überwacht werden. Ein Vertrauens nehmer kann ein Benutzerkonto, ein Gruppenkonto oder eine [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly)sein.

Verwenden Sie Funktionen, um den Inhalt von Sicherheits Deskriptoren, SIDs und ACLs zu manipulieren, anstatt direkt auf diese zuzugreifen. Dadurch wird sichergestellt, dass diese Strukturen syntaktisch genau bleiben und zukünftige Verbesserungen am Sicherheitssystem daran hindern, vorhandenen Code zu unterbrechen.

Die folgenden Themen enthalten Informationen zu Teilen des Zugriffs Steuerungs Modells:

-   [Zugriffs Token](access-tokens.md)
-   [Sicherheitsbeschreibungen](security-descriptors.md)
-   [Access Control Listen](access-control-lists.md)
-   [Access Control Einträge](access-control-entries.md)
-   [Zugriffsrechte und Zugriffs Masken](access-rights-and-access-masks.md)
-   [Funktionsweise von Access Check](how-dacls-control-access-to-an-object.md)
-   [Zentralisierte Autorisierungs Richtlinie](centralized-authorization-policy.md)
-   [Sicherheits-IDs](security-identifiers.md)

 

 
