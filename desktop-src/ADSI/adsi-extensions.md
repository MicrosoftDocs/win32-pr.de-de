---
title: ADSI-Erweiterungen
description: Eine ADSI-Erweiterung ist ein spezielles com-Objekt, mit dem ein Entwickler ein ADSI-Objekt erweitern kann.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- ADSI-Erweiterungen
- ADSI ADSI, using Extensions
- Erweiterungen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036327"
---
# <a name="adsi-extensions"></a><span data-ttu-id="7424e-106">ADSI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="7424e-106">ADSI Extensions</span></span>

<span data-ttu-id="7424e-107">Eine ADSI-Erweiterung ist ein spezielles com-Objekt, mit dem ein Entwickler ein ADSI-Objekt erweitern kann.</span><span class="sxs-lookup"><span data-stu-id="7424e-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="7424e-108">Jede Erweiterung ist einer angegebenen Klasse im Verzeichnis zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7424e-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="7424e-109">Mit diesem Erweiterungs Modell können Entwickler Methoden hinzufügen, um einem Objekt eine dynamischere Bedeutung zu verleihen.</span><span class="sxs-lookup"><span data-stu-id="7424e-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="7424e-110">In einem herkömmlichen Verzeichnis Programmiermodell erfolgt der Zugriff auf ein Objekt, indem die Objekt Attribute abgerufen und festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7424e-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="7424e-111">Mithilfe von ADSI Extensions können Sie einem Verzeichnis Objekt weitere Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7424e-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="7424e-112">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="7424e-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="7424e-113">Vorteile der Verwendung von ADSI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="7424e-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="7424e-114">ADSI-Erweiterungs Architektur</span><span class="sxs-lookup"><span data-stu-id="7424e-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="7424e-115">Integration von Erweiterungen durch ADSI</span><span class="sxs-lookup"><span data-stu-id="7424e-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="7424e-116">Was wird von einem Client angezeigt?</span><span class="sxs-lookup"><span data-stu-id="7424e-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="7424e-117">Erhalten von ADSI-Schnittstellen von ihrer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7424e-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="7424e-118">ADSI-Erweiterungstyp Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="7424e-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="7424e-119">Unterstützung für frühe Bindungen</span><span class="sxs-lookup"><span data-stu-id="7424e-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="7424e-120">Unterstützung späterer Bindungen</span><span class="sxs-lookup"><span data-stu-id="7424e-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="7424e-121">Iadsextension-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7424e-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="7424e-122">Unterstützung für duale Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7424e-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="7424e-123">Rebesuchen von com-Aggregations Regeln mit ADSI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="7424e-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="7424e-124">Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle unterstützen</span><span class="sxs-lookup"><span data-stu-id="7424e-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="7424e-125">Auflösung von Funktions-/Eigenschaftennamen-Konflikten bei der Automatisierung in Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="7424e-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




