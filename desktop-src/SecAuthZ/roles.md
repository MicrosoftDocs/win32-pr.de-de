---
description: Rollen dienen zwei unterschiedlichen Zwecken im Autorisierungs-Manager.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863019"
---
# <a name="roles"></a>Rollen

Rollen dienen zwei unterschiedlichen Zwecken im Autorisierungs-Manager. Eine Rolle besteht aus einer Reihe von Tasks oder Vorgängen, auf die eine Kategorie von Benutzern zugreifen muss. Außerdem handelt es sich um eine Gruppe von Benutzern und Gruppen, die in diese Kategorie passen.

-   [Rollen als Satz von Aufgaben](#roles-as-sets-of-tasks)
-   [Rollen als Gruppen von Benutzern und Gruppen](#roles-as-sets-of-users-and-groups)
-   [Zugehörige Themen](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Rollen als Satz von Aufgaben

Eine Autorisierungs Richtlinie weist [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekte einem [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt zu, um Aufgaben Sätze zu erstellen. Alle Benutzer und Gruppen, die diesem **iazrole** -Objekt zugewiesen sind, verfügen dann über die Berechtigung für den Zugriff auf alle Vorgänge, die von diesen **iaztask** -Objekten

Da ein [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt eine Reihe von Tasks und eine Gruppe von Benutzern und Gruppen mit Zugriff auf diese Aufgaben darstellt, bietet der Autorisierungs-Manager eine Möglichkeit, Rollen Definitionen zu erstellen, die mehreren **iazrole** -Objekten zugewiesen werden können. Ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt kann andere **iaztask** -Objekte enthalten. Anschließend können Sie dieses **iaztask** -Objekt als Rollendefinition verwenden, indem Sie es einem oder mehreren **iazrole** -Objekten zuweisen. Legen Sie [**die isroledefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) -Eigenschaft des **iaztask** -Objekts auf " **true** " fest, damit die Benutzeroberfläche des **Autorisierungs-Managers** für den MMC-Snap-in als Rolle angezeigt wird. 

## <a name="roles-as-sets-of-users-and-groups"></a>Rollen als Gruppen von Benutzern und Gruppen

Zuweisen von Benutzern und Gruppen zu einem [**iazrole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) -Objekt, um diesen Benutzern und Gruppen Zugriff auf die Aufgaben zu gewähren, die diesem **iazrole** -Objekt zugewiesen sind, indem die [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) -oder [**AddMembership Name**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) -Methode aufgerufen wird. Zuweisen vorhandener Anwendungs Gruppen, die durch [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekte dargestellt werden, zu einem **iazrole** -Objekt durch Aufrufen der [**addappmember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) -Methode. Alle Benutzer und Gruppen, die dem **iazrole** -Objekt zugewiesen sind, haben Zugriff auf die Aufgaben und Vorgänge, die dieser Rolle zugewiesen sind. Weitere Informationen zu Anwendungs Gruppen finden Sie unter [Benutzer und Gruppen](users-and-groups.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



