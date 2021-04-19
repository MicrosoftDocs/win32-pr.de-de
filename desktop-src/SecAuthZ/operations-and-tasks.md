---
description: Bei einem Vorgang handelt es sich um eine Computer Aktion auf niedriger Ebene.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Vorgänge und Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363587"
---
# <a name="operations-and-tasks"></a>Vorgänge und Aufgaben

Bei einem Vorgang handelt es sich um eine Computer Aktion auf niedriger Ebene. In der Autorisierungs-Manager-API wird ein Vorgang durch ein [**iazoperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) -Objekt dargestellt. Im Allgemeinen sind Vorgänge zu viele und zu niedrig, um die Verwaltung zu vereinfachen. Gruppieren von Vorgängen in Aufgaben zur Vereinfachung der Verwaltung von Autorisierungs Richtlinien.

Eine Aufgabe wird durch ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt dargestellt und kann ein oder mehrere [**iazoperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) -Objekte enthalten. Ein **iaztask** -Objekt kann auch andere **iaztask** -Objekte enthalten, sodass Aufgaben in den Netz Körper eingefügt werden können. Um die Verwaltung zu vereinfachen, sollte ein **iaztask** -Objekt eine Aufgabe darstellen, die ein echter Benutzer ausführen möchte.

Der Zugriff auf die Vorgänge, die in einer Aufgabe enthalten sind, kann zur Laufzeit durch ein Geschäftsregel Skript qualifiziert werden, das dem [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt zugeordnet ist, das diese Aufgabe darstellt. Weitere Informationen zu Geschäftsregel Skripts finden Sie [unter Geschäftsregeln](business-rules.md).

Ein [**iaztask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) -Objekt kann auch eine Rollendefinition darstellen, indem seine [**isroledefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) -Eigenschaft auf **true** festgelegt wird. Die MMC-Snap-in-Benutzeroberfläche des **Autorisierungs-Managers** zeigt dann dieses **iaztask** -Objekt als Rolle an. Weitere Informationen zu Rollen Definitionen finden Sie unter [Rollen](roles.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Definieren von Vorgängen in C++](defining-operations-in-c--.md)
</dt> <dt>

[Gruppieren von Vorgängen in Aufgaben in C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Benutzer und Gruppen](users-and-groups.md)
</dt> </dl>

 

 



