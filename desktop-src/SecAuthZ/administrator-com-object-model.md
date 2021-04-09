---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem ein Objekt mit Component Object Model erhöhten Rechten erstellt wird.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: COM-Objektmodell für Administratoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867224"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="ea0f3-103">COM-Objektmodell für Administratoren</span><span class="sxs-lookup"><span data-stu-id="ea0f3-103">Administrator COM Object Model</span></span>

<span data-ttu-id="ea0f3-104">Im COM-Objektmodell des Administrators führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge durch, die Administratorrechte erfordern, indem ein [Component Object Model](/windows/desktop/com/component-object-model--com--portal) Objekt mit erhöhten Rechten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ea0f3-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="ea0f3-105">Weitere Informationen zum Erstellen eines COM-Objekts mit erhöhten Rechten finden Sie [unter com-Erweiterungs Moniker](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="ea0f3-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="ea0f3-106">Ein Nachteil bei der Verwendung des com-Objektmodells für den Administrator ist, dass der Benutzer jedes Mal aufgefordert wird, wenn ein privilegierter Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea0f3-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="ea0f3-107">Jede Benutzeroberfläche, die das COM-Objekt steuern kann, muss vom COM-Objekt selbst dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ea0f3-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="ea0f3-108">Andernfalls könnte ein nicht privilegierter Prozess bewirken, dass das COM-Objekt mit erhöhten Berechtigungen privilegierte Vorgänge durchführt, ohne dass der Benutzer dazu aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ea0f3-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea0f3-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea0f3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea0f3-110">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="ea0f3-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="ea0f3-111">Administrator Broker Modell</span><span class="sxs-lookup"><span data-stu-id="ea0f3-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="ea0f3-112">Modell mit erhöhten Rechten</span><span class="sxs-lookup"><span data-stu-id="ea0f3-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="ea0f3-113">Betriebs System-Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="ea0f3-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
