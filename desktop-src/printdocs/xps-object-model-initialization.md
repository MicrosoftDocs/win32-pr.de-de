---
description: Beschreibt, wie ein XPS-OM initialisiert wird, das einem Programm das Erstellen eines XPS-Dokuments ermöglicht.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Initialisieren eines XPS-OMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344829"
---
# <a name="initialize-an-xps-om"></a><span data-ttu-id="5b63c-103">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="5b63c-103">Initialize an XPS OM</span></span>

<span data-ttu-id="5b63c-104">Beschreibt, wie ein XPS-OM initialisiert wird, das einem Programm das Erstellen eines XPS-Dokuments ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5b63c-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="5b63c-105">Die Schnittstellen der XPS-Dokument-API werden von einer [**ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) -Schnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b63c-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="5b63c-106">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf, um einen Zeiger auf eine **ixpsomobjectfactory** zu erhalten, die in Ihrem Programm verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b63c-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="5b63c-107">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5b63c-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="5b63c-108">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="5b63c-108">Code Example</span></span>

<span data-ttu-id="5b63c-109">Im folgenden Beispiel wird die Objektfactory erstellt, die zum Erstellen von XPS OM-Schnittstellen in anderen Beispielen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b63c-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a><span data-ttu-id="5b63c-110">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="5b63c-110">Best Practices</span></span>

<span data-ttu-id="5b63c-111">Sie können Ihr Programm effizienter gestalten, indem Sie einen Zeiger auf eine [**ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) -Schnittstelle erhalten, wenn Sie zum ersten Mal **ixpsomobjectfactory** aufrufen müssen, um eine Schnittstelle zu erstellen, und dann den Zeiger für die Verwendung in anderen Bereichen des Programms speichern.</span><span class="sxs-lookup"><span data-stu-id="5b63c-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="5b63c-112">Wenn das Programm die Objektfactory nicht mehr benötigt oder es für eine Weile nicht benötigt, kann der Zeiger freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b63c-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b63c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b63c-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5b63c-114">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="5b63c-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5b63c-115">Erstellen eines leeren XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="5b63c-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="5b63c-116">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="5b63c-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="5b63c-117">**Ixpsomobjectfactory**</span><span class="sxs-lookup"><span data-stu-id="5b63c-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="5b63c-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="5b63c-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="5b63c-119">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="5b63c-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5b63c-120">Verpackung</span><span class="sxs-lookup"><span data-stu-id="5b63c-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="5b63c-121">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="5b63c-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="5b63c-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5b63c-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
