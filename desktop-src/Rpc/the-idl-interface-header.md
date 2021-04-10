---
title: Der Header der IDL-Schnittstelle
description: Der IDL-Schnittstellen Header gibt Informationen zur Schnittstelle als Ganzes an. Anders als bei der ACF enthält der Schnittstellen Header Attribute, die plattformunabhängig sind.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102282"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="69b32-104">Der Header der IDL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="69b32-104">The IDL Interface Header</span></span>

<span data-ttu-id="69b32-105">Der IDL-Schnittstellen Header gibt Informationen zur Schnittstelle als Ganzes an.</span><span class="sxs-lookup"><span data-stu-id="69b32-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="69b32-106">Anders als bei der ACF enthält der Schnittstellen Header Attribute, die plattformunabhängig sind.</span><span class="sxs-lookup"><span data-stu-id="69b32-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="69b32-107">Attribute im Schnittstellen Header sind global für die gesamte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="69b32-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="69b32-108">Das heißt, Sie gelten für die-Schnittstelle und alle zugehörigen Teile.</span><span class="sxs-lookup"><span data-stu-id="69b32-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="69b32-109">Diese Attribute werden am Anfang der Schnittstellen Definition in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="69b32-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="69b32-110">Ein Beispiel wird in der folgenden Schnittstellen Definition angezeigt:</span><span class="sxs-lookup"><span data-stu-id="69b32-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="69b32-111">Beachten Sie, dass der Schnittstellen Header das **\[** [**UUID**](/windows/desktop/Midl/uuid) **\]** -Attribut und das **\[** [**Version**](/windows/desktop/Midl/version) - **\]** Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="69b32-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="69b32-112">Da diese die UUID und die Versionsnummer der-Schnittstelle darstellen, sind Sie Attribute der gesamten-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="69b32-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="69b32-113">Der Schnittstellen Text kann auch Attribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="69b32-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="69b32-114">Sie sind jedoch nicht auf die gesamte Schnittstelle anwendbar.</span><span class="sxs-lookup"><span data-stu-id="69b32-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="69b32-115">Sie verweisen auf bestimmte Elemente in der Schnittstelle, wie z. b. remote Prozedur Parameter.</span><span class="sxs-lookup"><span data-stu-id="69b32-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="69b32-116">Eine vollständige Erläuterung der IDL-Header Attribute finden Sie in der [Referenz zur Mittel l-Sprache](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="69b32-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 