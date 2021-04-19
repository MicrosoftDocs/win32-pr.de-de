---
description: Erzwingen der Aktivierung im Aufruferkontext
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Erzwingen der Aktivierung im Aufruferkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346432"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="fdabb-103">Erzwingen der Aktivierung im Kontext des Aufrufers</span><span class="sxs-lookup"><span data-stu-id="fdabb-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="fdabb-104">Sie können steuern, ob ein Objekt in seinem eigenen Kontext aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="fdabb-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="fdabb-105">Wenn Sie das Verwaltungs Programmkomponenten Dienste verwenden, um die Komponenten Aktivierung im Kontext des Aufrufers anzufordern, erfolgt Folgendes, wenn com+ eine Instanz der Komponente in einem Kontext aktiviert:</span><span class="sxs-lookup"><span data-stu-id="fdabb-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="fdabb-106">Wenn möglich, wird das-Objekt im Kontext des Erstellers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fdabb-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="fdabb-107">Die Objekt Aktivierung schlägt fehl, wenn ein eigener Kontext erforderlich ist. Der \_ \_ Versuch \_ , einen \_ \_ externen Client Kontext zu erstellen, \_ \_ wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdabb-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="fdabb-108">Ob das Objekt einen eigenen Kontext erfordert, hängt von seiner Konfiguration relativ zum aktuellen Zustand der Kontexteigenschaften des Aufrufers ab.</span><span class="sxs-lookup"><span data-stu-id="fdabb-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="fdabb-109">Weitere Details finden Sie unter [com+-Kontexte](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="fdabb-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="fdabb-110">Wenn ein anderer Aspekt des Objekts nicht ordnungsgemäß funktioniert, sollten Sie die Aktivierung auf dieser Ebene steuern.</span><span class="sxs-lookup"><span data-stu-id="fdabb-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="fdabb-111">Wenn die Komponente z. b. kein Marshalling unterstützt und Ihr eigener Kontext vorhanden ist, schlagen alle Aufrufe fehl, da Kontext übergreifende Aufrufe abgefangen und ein Lightweight-Marshal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdabb-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="fdabb-112">**So erzwingen Sie die Aktivierung im Kontext des Aufrufers**</span><span class="sxs-lookup"><span data-stu-id="fdabb-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="fdabb-113">Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente (befindet sich im Ordner **Komponenten** der ausgewählten COM+-Anwendung), für die Sie Aktivierungs Eigenschaften festlegen, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="fdabb-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="fdabb-114">Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .</span><span class="sxs-lookup"><span data-stu-id="fdabb-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="fdabb-115">Aktivieren Sie das Kontrollkästchen **muss im Kontext des aufruferaufrufern aktiviert werden** .</span><span class="sxs-lookup"><span data-stu-id="fdabb-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="fdabb-116">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdabb-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdabb-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fdabb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdabb-118">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="fdabb-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="fdabb-119">Erzwingen der Aktivierung im Standardkontext</span><span class="sxs-lookup"><span data-stu-id="fdabb-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



