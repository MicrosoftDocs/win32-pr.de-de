---
title: Die Wire_marshal-und user_marshal Attribute
description: In diesem Abschnitt wird die Implementierung der Konvertierung von programmierdatentypen mithilfe der Attribute "Mittel" \ "Wire \_ Marshal \" und "\ User \_ Marshal \" erläutert
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039404"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="3beb3-103">Die Attribute "Wire \_ Marshal" und "User \_ Marshal"</span><span class="sxs-lookup"><span data-stu-id="3beb3-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="3beb3-104">In diesem Abschnitt wird die Implementierung der Konvertierung von Programmier Datentypen mithilfe der Attribute "Mittel l \[ - [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] " erläutert</span><span class="sxs-lookup"><span data-stu-id="3beb3-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="3beb3-105">Die Informationen werden in den folgenden Abschnitten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3beb3-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="3beb3-106">Das Wire \_ Marshal-Attribut</span><span class="sxs-lookup"><span data-stu-id="3beb3-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="3beb3-107">Das Mars-Attribut des Benutzers \_</span><span class="sxs-lookup"><span data-stu-id="3beb3-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="3beb3-108">Die Type \_ usersize-Funktion</span><span class="sxs-lookup"><span data-stu-id="3beb3-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="3beb3-109">Der Typ \_ usermarshal-Funktion</span><span class="sxs-lookup"><span data-stu-id="3beb3-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="3beb3-110">Der Typ \_ userunmarshal-Funktion</span><span class="sxs-lookup"><span data-stu-id="3beb3-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="3beb3-111">Die Type \_ userfree-Funktion</span><span class="sxs-lookup"><span data-stu-id="3beb3-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="3beb3-112">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="3beb3-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 