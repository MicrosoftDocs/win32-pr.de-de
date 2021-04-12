---
description: Eine Komponente mit mindestens einer Warteschlangen Schnittstelle ist eine in der Warteschlange befindliche Komponente.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Erstellen von Warteschlangen fähigen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393073"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="0b0db-103">Erstellen von Warteschlangen fähigen Komponenten</span><span class="sxs-lookup"><span data-stu-id="0b0db-103">Creating Queuable Components</span></span>

<span data-ttu-id="0b0db-104">Eine Komponente mit mindestens einer Warteschlangen Schnittstelle ist eine in der *Warteschlange befindliche Komponente*.</span><span class="sxs-lookup"><span data-stu-id="0b0db-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="0b0db-105">Damit eine Komponente von einer Warteschlange aufgerufen werden kann, müssen die Schnittstellen als in die Warteschlange eingereiht werden, und die Komponente muss in einer Anwendung in der Warteschlange installiert sein.</span><span class="sxs-lookup"><span data-stu-id="0b0db-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="0b0db-106">Eine in der Warteschlange befindliche Komponente kann jedoch eine Komponente einer Anwendung sein, die keine Warteschlange ist.</span><span class="sxs-lookup"><span data-stu-id="0b0db-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="0b0db-107">Eine queuable-Schnittstelle darf nur in-Parameter enthalten – keine out-Parameter und keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="0b0db-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="0b0db-108">Diese Eigenschaften werden durch die Analyse der Typinformationen während der Installation von Komponenten überprüft.</span><span class="sxs-lookup"><span data-stu-id="0b0db-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="0b0db-109">Wenn die Schnittstelle nicht in die Warteschlange eingereiht werden kann, kann die Warteschlange der Anwendung mit der Komponente nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0b0db-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="0b0db-110">Um eine COM+-Schnittstelle als Warteschlange anzugeben, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0b0db-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="0b0db-111">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="0b0db-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="0b0db-112">Öffnen Sie den Ordner **Interfaces** der Komponente der com+-Anwendung, die Sie in die Warteschlange stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0b0db-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="0b0db-113">Klicken Sie mit der rechten Maustaste auf die Schnittstelle, die Sie als Warteschlange markieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="0b0db-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="0b0db-114">Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.</span><span class="sxs-lookup"><span data-stu-id="0b0db-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="0b0db-115">Aktivieren Sie das Kontrollkästchen mit der Bezeichnung **Warteschlange**.</span><span class="sxs-lookup"><span data-stu-id="0b0db-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="0b0db-116">Wenn das Kontrollkästchen in der **Warteschlange abgeblendet** ist, erfüllt die Schnittstelle nicht die oben beschriebenen Warteschlangen Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="0b0db-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="0b0db-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0db-117">Click **OK**.</span></span>

    <span data-ttu-id="0b0db-118">Eine in die Warteschlange einsetzbare Komponente kann als solche identifiziert werden, indem dem Schnittstellen Abschnitt der IDL-Quelldatei (Interface Definition Language) für alle Schnittstellen, die in die Warteschlange eingereiht werden können, das queuable-Attribut Makro</span><span class="sxs-lookup"><span data-stu-id="0b0db-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="0b0db-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b0db-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0db-120">Komponenten Warteschlangen erstellen</span><span class="sxs-lookup"><span data-stu-id="0b0db-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="0b0db-121">Entwickeln von Komponenten in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="0b0db-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



