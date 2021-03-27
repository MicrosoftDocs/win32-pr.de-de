---
description: Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um eine automatische Wiedergabe zu verhindern.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Verhindern von AutoPlay für eine Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979529"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="7cc58-103">Verhindern von AutoPlay für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="7cc58-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="7cc58-104">Veranschaulicht, welcher Registrierungsschlüssel festgelegt werden muss, um eine automatische Wiedergabe zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7cc58-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="7cc58-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="7cc58-105">Instructions</span></span>


<span data-ttu-id="7cc58-106">Fügen Sie den folgenden **reg \_ SZ** -Wert hinzu, um zu verhindern, dass die Wiedergabe als Reaktion auf ein Ereignis gestartet wird, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7cc58-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="7cc58-107">Der Wert ist der Klassen Bezeichner (CLSID), der von der Komponente, die das Ereignis erstellt, in der laufenden Objekttabelle (rot) bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7cc58-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="7cc58-108">Der Wert enthält keine Daten.</span><span class="sxs-lookup"><span data-stu-id="7cc58-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7cc58-109">Unter diesem Schlüssel werden die CLSIDs nicht in geschweifte Klammern ( {} ) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7cc58-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



