---
description: In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf Seiten Verweise in einem XPS-OM ermöglichen.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Arbeiten mit ixpsompagereferenzierungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865864"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="70328-103">Arbeiten mit ixpsompagereferenzierungsschnittstellen</span><span class="sxs-lookup"><span data-stu-id="70328-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="70328-104">In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf Seiten Verweise in einem XPS-OM ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="70328-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="70328-105">Schnittstellen Name</span><span class="sxs-lookup"><span data-stu-id="70328-105">Interface name</span></span>                                                  | <span data-ttu-id="70328-106">Logische untergeordnete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="70328-106">Logical child interfaces</span></span>                    | <span data-ttu-id="70328-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70328-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70328-108">**Ixpsompagereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="70328-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="70328-109">**Ixpsompage**</span><span class="sxs-lookup"><span data-stu-id="70328-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="70328-110">Virtualisiert den Inhalt einer Dokument Seite.</span><span class="sxs-lookup"><span data-stu-id="70328-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="70328-111">Ein Seiten Verweis enthält grundlegende Informationen über die Seite, einige Seiteneigenschaften und einen Link zum Seiten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="70328-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="70328-112">Die [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle, die Seiteninhalte umfasst, wird von der [**ixpsompagereferen:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70328-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="70328-113">**Ixpsomnamecollection**</span><span class="sxs-lookup"><span data-stu-id="70328-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="70328-114">Keine</span><span class="sxs-lookup"><span data-stu-id="70328-114">None</span></span><br/>                             | <span data-ttu-id="70328-115">Enthält eine Liste von Seitenelementen, bei denen es sich um Linkziele handelt.</span><span class="sxs-lookup"><span data-stu-id="70328-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="70328-116">Die Liste wird von der [**ixpsompagereferen:: collectlinktargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70328-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="70328-117">**Ixpsomparametresources**</span><span class="sxs-lookup"><span data-stu-id="70328-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="70328-118">Keine</span><span class="sxs-lookup"><span data-stu-id="70328-118">None</span></span><br/>                             | <span data-ttu-id="70328-119">Enthält eine Liste der teilbasierten Ressourcen, die der Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70328-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="70328-120">Diese Liste wird von der [**ixpsompagereferen:: collectsamtresources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70328-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="70328-121">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="70328-121">Code Examples</span></span>

<span data-ttu-id="70328-122">Die folgenden Codebeispiele veranschaulichen die Arbeit mit den Seiten Verweis Schnittstellen in einem Programm.</span><span class="sxs-lookup"><span data-stu-id="70328-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="70328-123">Inhalt der Seite erhalten</span><span class="sxs-lookup"><span data-stu-id="70328-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="70328-124">Hiermit wird die Liste der Hyperlink-Ziele auf dieser Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70328-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="70328-125">Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70328-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="70328-126">Inhalt der Seite erhalten</span><span class="sxs-lookup"><span data-stu-id="70328-126">Get the page contents</span></span>

<span data-ttu-id="70328-127">Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle abgerufen, die den Seiten Inhalt umfasst.</span><span class="sxs-lookup"><span data-stu-id="70328-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="70328-128">Wenn die Seite nicht in das XPS-OM geladen wurde [**, wird die**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) Seite in das XPS-OM geladen, wenn das XPS-OM durch Aufrufen von [**ixpsomobjectfactory:: createpackagefromfile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile)initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="70328-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="70328-129">Hiermit wird die Liste der Hyperlink-Ziele auf dieser Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70328-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="70328-130">Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) -Schnittstelle abgerufen, die die Liste der Seitenelemente enthält, die Hyperlink-Ziele sind.</span><span class="sxs-lookup"><span data-stu-id="70328-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="70328-131">Wenn die Seite nicht in das XPS-OM geladen wurde, wird die Liste der Hyperlink-Ziele aus dem Markup **Page Content. LinkTargets** gelesen.</span><span class="sxs-lookup"><span data-stu-id="70328-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="70328-132">Wenn die Seite geladen wurde, überprüft [**collectlinktargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) jedes Element auf der Seite und gibt eine Liste von Elementen zurück, deren **ishyperlinktarget** -Attribut " **true**" ist.</span><span class="sxs-lookup"><span data-stu-id="70328-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="70328-133">Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="70328-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="70328-134">Im folgenden Codebeispiel werden die Listen der verschiedenen Ressourcen abgerufen, die von dieser Seite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70328-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );
```



## <a name="related-topics"></a><span data-ttu-id="70328-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70328-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70328-136">**Ixpsomnamecollection**</span><span class="sxs-lookup"><span data-stu-id="70328-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="70328-137">**Ixpsompage**</span><span class="sxs-lookup"><span data-stu-id="70328-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="70328-138">**Ixpsompagereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="70328-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="70328-139">**Ixpsomparametresources**</span><span class="sxs-lookup"><span data-stu-id="70328-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="70328-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="70328-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




