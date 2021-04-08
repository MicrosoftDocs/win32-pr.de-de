---
title: Abrufen von untergeordneten IDs durch Clients
description: Abrufen von untergeordneten IDs durch Clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727721"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="c0459-103">Abrufen von untergeordneten IDs durch Clients</span><span class="sxs-lookup"><span data-stu-id="c0459-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="c0459-104">Client Entwickler können die untergeordnete ID eines Objekts auf folgende Weise erhalten:</span><span class="sxs-lookup"><span data-stu-id="c0459-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="c0459-105">" [**Accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0459-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="c0459-106">Diese Funktion Ruft ein Array von [**Variant**](variant-structure.md) -Strukturen ab.</span><span class="sxs-lookup"><span data-stu-id="c0459-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="c0459-107">Fragen Sie das-Objekt ab, um festzustellen, ob es die [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c0459-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="c0459-108">Wenn Sie vorhanden ist, verwenden Sie [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) Abruf untergeordneter IDs.</span><span class="sxs-lookup"><span data-stu-id="c0459-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="c0459-109">Erfassen Sie die untergeordneten IDs, indem Sie die [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) -Methode des übergeordneten Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c0459-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="c0459-110">Der Client ist dafür verantwortlich, den für die [**Variant**](variant-structure.md) -Strukturen genutzten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c0459-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="c0459-111">Clients müssen auch [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für jede zurückgegebene [**IDispatch**](idispatch-interface.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="c0459-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 