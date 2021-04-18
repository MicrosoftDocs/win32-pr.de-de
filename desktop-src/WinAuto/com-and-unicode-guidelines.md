---
title: COM-und Unicode-Richtlinien
description: Da Microsoft Active Accessibility auf Component Object Model (com) basiert, benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und-Schnittstellen, und Sie müssen wissen, wie Sie grundlegende Aufgaben ausführen (z. b. die Initialisierung der com-Bibliothek).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338269"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="fa637-103">COM-und Unicode-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fa637-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="fa637-104">Da Microsoft Active Accessibility auf Component Object Model (com) basiert, benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und-Schnittstellen, und Sie müssen wissen, wie Sie grundlegende Aufgaben ausführen (z. b. die Initialisierung der com-Bibliothek).</span><span class="sxs-lookup"><span data-stu-id="fa637-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="fa637-105">Server Entwickler müssen wissen, wie Klassen entworfen werden, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, und wie barrierefreie Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fa637-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="fa637-106">Außerdem benötigen Sie ein mittleres Maß an Verständnis von Unicode, um viele der Funktionen von Microsoft Active Accessibility zu verwenden, die Zeichen folgen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fa637-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="fa637-107">Um Microsoft Active Accessibility effektiv zu verwenden, sollten Sie die folgenden com-und Unicode-Funktionen, Strukturen, Datentypen und Schnittstellen kennen.</span><span class="sxs-lookup"><span data-stu-id="fa637-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="fa637-108">Informationen zu einigen dieser Elemente finden Sie in dieser Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="fa637-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="fa637-109">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="fa637-109">Functions:</span></span>

-   [<span data-ttu-id="fa637-110">**OleInitialize**</span><span class="sxs-lookup"><span data-stu-id="fa637-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="fa637-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="fa637-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="fa637-112">[**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="fa637-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="fa637-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) und [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="fa637-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="fa637-114">" [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) " und " [ **WideCharToMultiByte** "](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="fa637-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="fa637-115">" [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) " und " [ **sysfrestring** "](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="fa637-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="fa637-116">Strukturen und Datentypen:</span><span class="sxs-lookup"><span data-stu-id="fa637-116">Structures and data types:</span></span>

-   [<span data-ttu-id="fa637-117">**Konfigur**</span><span class="sxs-lookup"><span data-stu-id="fa637-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="fa637-118">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa637-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="fa637-119">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="fa637-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="fa637-120">COM-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="fa637-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="fa637-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="fa637-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="fa637-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="fa637-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="fa637-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="fa637-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="fa637-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fa637-124">In this section</span></span>

-   [<span data-ttu-id="fa637-125">VARIANT-Struktur</span><span class="sxs-lookup"><span data-stu-id="fa637-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="fa637-126">IDispatch-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fa637-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="fa637-127">Unicode und ANSI-Zeichen folgen werden umgerechnet</span><span class="sxs-lookup"><span data-stu-id="fa637-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 