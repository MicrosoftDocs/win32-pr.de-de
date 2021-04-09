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
# <a name="working-with-ixpsompagereference-interfaces"></a>Arbeiten mit ixpsompagereferenzierungsschnittstellen

In diesem Thema wird beschrieben, wie Sie die Schnittstellen verwenden, die den Zugriff auf Seiten Verweise in einem XPS-OM ermöglichen.



| Schnittstellen Name                                                  | Logische untergeordnete Schnittstellen                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Virtualisiert den Inhalt einer Dokument Seite. <br/> Ein Seiten Verweis enthält grundlegende Informationen über die Seite, einige Seiteneigenschaften und einen Link zum Seiten Inhalt. Die [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle, die Seiteninhalte umfasst, wird von der [**ixpsompagereferen:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) -Methode zurückgegeben.<br/> |
| [**Ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | Keine<br/>                             | Enthält eine Liste von Seitenelementen, bei denen es sich um Linkziele handelt. Die Liste wird von der [**ixpsompagereferen:: collectlinktargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) -Methode zurückgegeben.<br/>                                                                                                                                                               |
| [**Ixpsomparametresources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | Keine<br/>                             | Enthält eine Liste der teilbasierten Ressourcen, die der Seite zugeordnet sind. Diese Liste wird von der [**ixpsompagereferen:: collectsamtresources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) -Methode zurückgegeben.<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele veranschaulichen die Arbeit mit den Seiten Verweis Schnittstellen in einem Programm.

-   [Inhalt der Seite erhalten](#get-the-page-contents)
-   [Hiermit wird die Liste der Hyperlink-Ziele auf dieser Seite angezeigt.](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Inhalt der Seite erhalten

Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle abgerufen, die den Seiten Inhalt umfasst. Wenn die Seite nicht in das XPS-OM geladen wurde [**, wird die**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) Seite in das XPS-OM geladen, wenn das XPS-OM durch Aufrufen von [**ixpsomobjectfactory:: createpackagefromfile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile)initialisiert wird.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Hiermit wird die Liste der Hyperlink-Ziele auf dieser Seite angezeigt.

Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) -Schnittstelle abgerufen, die die Liste der Seitenelemente enthält, die Hyperlink-Ziele sind. Wenn die Seite nicht in das XPS-OM geladen wurde, wird die Liste der Hyperlink-Ziele aus dem Markup **Page Content. LinkTargets** gelesen. Wenn die Seite geladen wurde, überprüft [**collectlinktargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) jedes Element auf der Seite und gibt eine Liste von Elementen zurück, deren **ishyperlinktarget** -Attribut " **true**" ist.


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Hiermit werden die Teil Ressourcen angezeigt, die dieser Seite zugeordnet sind.

Im folgenden Codebeispiel werden die Listen der verschiedenen Ressourcen abgerufen, die von dieser Seite verwendet werden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**Ixpsomparametresources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




