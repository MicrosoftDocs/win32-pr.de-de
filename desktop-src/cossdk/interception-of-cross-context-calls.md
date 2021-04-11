---
description: Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontext Grenze hinweg.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Abfangen von Kontext übergreifenden aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342259"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="f88e0-103">Abfangen von Kontext übergreifenden aufrufen</span><span class="sxs-lookup"><span data-stu-id="f88e0-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="f88e0-104">Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontext Grenze hinweg.</span><span class="sxs-lookup"><span data-stu-id="f88e0-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="f88e0-105">Aufrufe über die Kontext Grenze werden mit Lightweight-Proxys verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f88e0-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="f88e0-106">Diese Proxys verarbeiten jede beliebige Vermittlung, die erforderlich ist, um die Laufzeitumgebung von einer zu ändern, die den Aufrufer an den aufgerufenen anpasst.</span><span class="sxs-lookup"><span data-stu-id="f88e0-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="f88e0-107">Dieser Prozess wird als *Abfang* Funktion bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f88e0-107">This process is known as *interception*.</span></span>

<span data-ttu-id="f88e0-108">Eine Kontext übergreifende Aufruf Abfang Funktion ist erforderlich, da Objekte in verschiedenen Kontexten unterschiedliche Lauf Zeitanforderungen haben – dies ist genau der Grund für den Kontext.</span><span class="sxs-lookup"><span data-stu-id="f88e0-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="f88e0-109">Com+ fängt alle Objekt Verweise ab, die Sie als Methoden Parameter übergeben, und konvertiert sie automatisch in Proxys, sodass Sie im neuen Kontext verwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="f88e0-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="f88e0-110">Wenn Sie Objekt Verweise über Kontext Grenzen hinweg auf andere Weise freigeben, z. –. in globalen Variablen – sollten Sie immer [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) und [**zählmarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)verwenden.</span><span class="sxs-lookup"><span data-stu-id="f88e0-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="f88e0-111">Diese Funktionen können einen Objekt Verweis in einen Proxy übersetzen, der in einem anderen Kontext verwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="f88e0-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="f88e0-112">Geben Sie niemals einen Rohdaten Objekt Verweis über Kontext Grenzen hinweg frei.</span><span class="sxs-lookup"><span data-stu-id="f88e0-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="f88e0-113">Das Verhalten von Aufrufen über den Kontext hinweg kann bei Objekten, die Schnittstellen bereitstellen, die nicht gemarshallt werden können, unerwünschte Folgen haben.</span><span class="sxs-lookup"><span data-stu-id="f88e0-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="f88e0-114">In diesem Fall möchten Sie wahrscheinlich darauf hinweisen, dass das Objekt, das nicht gemarshallt werden kann, nur im Kontext seines Aufrufers und nie in seinem eigenen Kontext aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f88e0-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="f88e0-115">Wählen Sie hierzu auf der Seite Komponenten **Eigenschaften** auf der Registerkarte **Aktivierung** die Option muss in der Kontext Option des **Aufrufers aktiviert sein** aus.</span><span class="sxs-lookup"><span data-stu-id="f88e0-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="f88e0-116">(Eine Schritt-für-Schritt-Anleitung finden Sie [unter Erzwingen der Aktivierung im Kontext des Aufrufers](enforcing-activation-in-the-caller-s-context.md) .)</span><span class="sxs-lookup"><span data-stu-id="f88e0-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f88e0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f88e0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88e0-118">Kontext Aktivierung</span><span class="sxs-lookup"><span data-stu-id="f88e0-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
