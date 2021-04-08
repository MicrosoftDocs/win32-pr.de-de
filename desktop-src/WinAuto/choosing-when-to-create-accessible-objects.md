---
title: Auswählen, wann barrierefreie Objekte erstellt werden sollen
description: Server Entwickler können alle zugänglichen Objekte in einem Container erstellen, wenn der Container erstellt wird, oder Sie können die barrierefreien Objekte dynamisch erstellen.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037254"
---
# <a name="choosing-when-to-create-accessible-objects"></a><span data-ttu-id="ffa04-103">Auswählen, wann barrierefreie Objekte erstellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="ffa04-103">Choosing When to Create Accessible Objects</span></span>

<span data-ttu-id="ffa04-104">Server Entwickler können alle zugänglichen Objekte in einem Container erstellen, wenn der Container erstellt wird, oder Sie können die barrierefreien Objekte dynamisch erstellen.</span><span class="sxs-lookup"><span data-stu-id="ffa04-104">Server developers can create all the accessible objects within a container when the container is created, or they can create the accessible objects dynamically.</span></span>

<span data-ttu-id="ffa04-105">Stellen Sie sich z. b. ein Dialogfeld mit mehreren benutzerdefinierten Steuerelementen vor.</span><span class="sxs-lookup"><span data-stu-id="ffa04-105">For example, imagine a dialog box with several custom controls.</span></span> <span data-ttu-id="ffa04-106">Ein Server erstellt barrierefreie Objekte für alle benutzerdefinierten Steuerelemente, wenn das Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ffa04-106">A server creates accessible objects for all of the custom controls when the dialog box is displayed.</span></span> <span data-ttu-id="ffa04-107">Wenn eines der Steuerelemente jedoch ein benutzerdefiniertes Kombinations Feld ist, wartet der Server, bis ein Benutzer es auswählt, um barrierefreie Objekte für die im Kombinations Feld enthaltenen Elemente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ffa04-107">However, if one of the controls is a custom combo box, the server waits until a user selects it to create accessible objects for the items that the combo box contains.</span></span>

<span data-ttu-id="ffa04-108">Wenn das übergeordnete Objekt barrierefreie Objekte dynamisch erstellt, wird weniger Arbeitsspeicher verwendet, als wenn alle möglichen zugänglichen Objekte im Voraus erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ffa04-108">By having the parent create accessible objects dynamically, applications use less memory than if all the possible accessible objects were created ahead of time.</span></span>

 

 




