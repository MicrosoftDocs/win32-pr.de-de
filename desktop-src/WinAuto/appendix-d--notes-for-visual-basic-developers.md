---
title: Anhang D Hinweise für Visual Basic-Entwickler
description: Dieser Abschnitt enthält Informationen zu Microsoft-Active Accessibility für Entwickler von Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947660"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="5d360-103">Anhang D: Hinweise für Visual Basic-Entwickler</span><span class="sxs-lookup"><span data-stu-id="5d360-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="5d360-104">Dieser Abschnitt enthält Informationen zu Microsoft-Active Accessibility für Entwickler von Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5d360-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="5d360-105">In Visual Basic geschriebene Anwendungen sind Microsoft Active Accessibility-Clients.</span><span class="sxs-lookup"><span data-stu-id="5d360-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="5d360-106">Sie stellen keine Informationen über Ihre benutzerdefinierten Benutzeroberflächen Elemente bereit, da Sie [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) oder keine andere Component Object Model (com)-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="5d360-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="5d360-107">In dieser Dokumentation werden die C/C++-Namen für die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften verwendet; die Visual Basic Namen sind jedoch ähnlich.</span><span class="sxs-lookup"><span data-stu-id="5d360-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="5d360-108">Beispielsweise würde die Eigenschaft [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) in einer Visual Basic Anwendung als **accName** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5d360-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5d360-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5d360-109">In this section</span></span>

-   [<span data-ttu-id="5d360-110">Hinweise zur Visual Basic-Methode: accName</span><span class="sxs-lookup"><span data-stu-id="5d360-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="5d360-111">Hinweise zur Visual Basic-Methode: accValue</span><span class="sxs-lookup"><span data-stu-id="5d360-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="5d360-112">Visual Basic Beispiel Programme</span><span class="sxs-lookup"><span data-stu-id="5d360-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 




