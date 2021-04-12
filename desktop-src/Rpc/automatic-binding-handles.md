---
title: Automatische Bindungs Handles
description: Automatische Bindungs Handles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen dem Client und dem Server beibehalten werden müssen.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316113"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="41700-103">Automatische Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="41700-103">Automatic Binding Handles</span></span>

<span data-ttu-id="41700-104">Automatische Bindungs Handles sind nützlich, wenn die Anwendung keinen bestimmten Server benötigt und keine Zustandsinformationen zwischen dem Client und dem Server beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="41700-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="41700-105">Wenn Sie ein automatisches Bindungs Handle verwenden, müssen Sie keinen Client Anwendungscode für die Behandlung von Bindungen und Handles schreiben – Sie geben einfach die Verwendung des automatischen Bindungs Handles in der Anwendungs Konfigurationsdatei (ACF) an.</span><span class="sxs-lookup"><span data-stu-id="41700-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="41700-106">Der Stub definiert dann das Handle und verwaltet die Bindung.</span><span class="sxs-lookup"><span data-stu-id="41700-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="41700-107">Beispielsweise kann ein Zeitstempel Vorgang mithilfe eines automatischen Handles implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="41700-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="41700-108">Es gibt keinen Unterschied zur Client Anwendung, welcher Server den Zeitstempel bereitstellt, da er die Zeit von einem beliebigen verfügbaren Server annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="41700-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="41700-109">Automatische Handles werden für die Macintosh-Plattform nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41700-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="41700-110">Sie geben die Verwendung von automatischen Handles an, indem Sie das Attribut für \[ [**Automatisches \_ handle**](/windows/desktop/Midl/auto-handle) \] in der ACF einschließen.</span><span class="sxs-lookup"><span data-stu-id="41700-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="41700-111">Im Zeitstempel Beispiel wird die folgende ACF verwendet:</span><span class="sxs-lookup"><span data-stu-id="41700-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="41700-112">Wenn die ACF kein anderes handle-Attribut enthält, und wenn die Remote Prozeduren keine expliziten Handles verwenden, verwendet der mittlerer l-Compiler standardmäßig automatische Handles.</span><span class="sxs-lookup"><span data-stu-id="41700-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="41700-113">Außerdem werden automatische Handles als Standard verwendet, wenn die ACF nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41700-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="41700-114">Die Remote Prozeduren werden in der IDL-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="41700-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="41700-115">Das automatische Handle darf nicht als Argument für die Remote Prozedur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="41700-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="41700-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="41700-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="41700-117">Der Vorteil des automatischen Handles besteht darin, dass der Entwickler keinen Code zum Verwalten des Handles schreiben muss. die stusb verwalten die Bindung automatisch.</span><span class="sxs-lookup"><span data-stu-id="41700-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="41700-118">Dies unterscheidet sich erheblich von dem [Hello, World-Beispiel](tutorial.md), bei dem der Client das implizite primitive Handle verwaltet, das in der ACF definiert ist, und mehrere Lauf Zeitfunktionen zum Einrichten des Bindungs Handles aufruft.</span><span class="sxs-lookup"><span data-stu-id="41700-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 