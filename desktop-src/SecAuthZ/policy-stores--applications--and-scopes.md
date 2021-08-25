---
description: Autorisierungsrichtlinienspeicher, Anwendungen und Bereiche stellen unterschiedliche Organisationsebenen der Autorisierungs-Manager-Richtlinie dar.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Richtlinienspeicher, Anwendungen und Bereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db06b291ef81f391fed1a0094b73c9b31d0342f59bce22d93779c7bfa48a80b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907570"
---
# <a name="policy-stores-applications-and-scopes"></a>Richtlinienspeicher, Anwendungen und Bereiche

Autorisierungsrichtlinienspeicher, Anwendungen und Bereiche stellen unterschiedliche Organisationsebenen der Autorisierungs-Manager-Richtlinie dar. Ein Richtlinienspeicher kann eine oder mehrere Anwendungen enthalten, und eine Anwendung kann einen oder mehrere Bereiche enthalten.

-   [Autorisierungsrichtlinienspeicher](#authorization-policy-stores)
-   [Anwendungen](#policy-stores-applications-and-scopes)
-   [Bereiche](#policy-stores-applications-and-scopes)
-   [Delegierung](#delegation)
-   [Zugehörige Themen](#related-topics)

## <a name="authorization-policy-stores"></a>Autorisierungsrichtlinienspeicher

In der Autorisierungs-Manager-API wird ein Autorisierungsrichtlinienspeicher durch ein [**IAzAuthorizationStore-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) dargestellt. Der Autorisierungsrichtlinienspeicher enthält Definitionen und Zuweisungen von Anwendungen, Geltungsbereichen, Vorgängen, Aufgaben, Rollen und Benutzergruppen.

Ein Autorisierungsrichtlinienspeicher kann entweder als XML-Datei oder in Active Directory gespeichert werden.

Eine Anwendung muss einen Autorisierungsrichtlinienspeicher initialisieren, bevor Informationen im Speicher geändert oder die Speicherrichtlinie verwendet wird, um den Clientzugriff auf Ressourcen zu überprüfen.

Ein Autorisierungsrichtlinienspeicher kann ein oder mehrere [**IAzApplication-Objekte**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) enthalten, die jeweils die Autorisierungsrichtlinie für eine bestimmte Anwendung darstellen.

## <a name="applications"></a>Anwendungen

In der Autorisierungs-Manager-API wird eine Anwendung durch ein [**IAzApplication-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) dargestellt. Ein Autorisierungsrichtlinienspeicher kann Autorisierungsrichtlinieninformationen für viele Anwendungen enthalten. Mithilfe **von IAzApplication-Objekten** können Sie verschiedene Autorisierungsrichtlinien für verschiedene Anwendungen in einem einzigen Richtlinienspeicher speichern.

Ein Autorisierungsrichtlinienspeicher muss mindestens eine Anwendung enthalten.

## <a name="scopes"></a>Bereiche

In der Autorisierungs-Manager-API wird ein Bereich durch ein [**IAzScope-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazscope) dargestellt. Bereiche stellen eine zusätzliche, optionale Organisationsebene für eine Autorisierungsrichtlinie zur Verfügung. Eine Anwendung kann einen oder mehrere Bereiche enthalten, muss aber keines enthalten (Der Autorisierungs-Manager stellt einen anwendungsweiten Standardbereich zur Auswahl).

Ein Bereich ist eine Unterteilung innerhalb einer Anwendung, die Ressourcen von anderen Ressourcen trennt, die von dieser Anwendung verwendet werden. Wenn Sie über Autorisierungs-Manager-Gruppen, Rollenzuweisungen, Rollendefinitionen oder Aufgabendefinitionen verfügen, die Sie nicht auf eine gesamte Anwendung anwenden möchten, können Sie sie auf Bereichsebene erstellen.

## <a name="delegation"></a>Delegierung

Autorisierungsrichtlinienspeicher, die in Active Directory gespeichert sind, unterstützen die Delegierung der Verwaltung. Die Verwaltung kann an Benutzer und Gruppen auf Store-, Anwendungs- oder Bereichsebene delegiert werden. Jede Ebene definiert Administratorrollen für die Richtlinie auf dieser Ebene. Um die Steuerung an einen Benutzer oder eine Gruppe zu delegieren, weisen Sie sie der Administratorrolle zu. Um einem Benutzer oder einer Gruppe das Lesen der Richtlinie zu ermöglichen, weisen Sie sie der Rolle Leser zu.

Administratoren eines Speichers, einer Anwendung oder eines Bereichs können den Richtlinienspeicher auf delegierter Ebene lesen und ändern. Leser können den Richtlinienspeicher auf delegierter Ebene lesen, aber den Speicher nicht ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Autorisierungsrichtlinien-Store-Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Erstellen eines Anwendungsobjekts in C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delegieren der Definition von Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



