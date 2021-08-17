---
description: In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die den Zugriff auf Seitenverweise in einem XPS OM ermöglichen.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Arbeiten mit IXpsOMPageReference-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee38856075a967fbf0f66255c922e181961dc42f1214f75e05da7d4062d6c4a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098682"
---
# <a name="working-with-ixpsompagereference-interfaces"></a>Arbeiten mit IXpsOMPageReference-Schnittstellen

In diesem Thema wird beschrieben, wie die Schnittstellen verwendet werden, die den Zugriff auf Seitenverweise in einem XPS OM ermöglichen.



| Schnittstellenname                                                  | Logische untergeordnete Schnittstellen                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Virtualisiert den Inhalt einer Dokumentseite. <br/> Ein Seitenverweis enthält grundlegende Informationen über die Seite, einige Seiteneigenschaften und einen Link zum Seiteninhalt. Die [**IXpsOMPage-Schnittstelle,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) die Seiteninhalte umfasst, wird von der [**IXpsOMPageReference::GetPage-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) zurückgegeben.<br/> |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | Keine<br/>                             | Enthält eine Liste von Seitenelementen, die Linkziele sind. Die Liste wird von der [**IXpsOMPageReference::CollectLinkTargets-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) zurückgegeben.<br/>                                                                                                                                                               |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | Keine<br/>                             | Enthält eine Liste der teilbasierten Ressourcen, die der Seite zugeordnet sind. Diese Liste wird von der [**IXpsOMPageReference::CollectPartResources-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) zurückgegeben.<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele veranschaulichen die Arbeit mit den Seitenverweisschnittstellen in einem Programm.

-   [Anzeigen des Seiteninhalts](#get-the-page-contents)
-   [Abrufen der Liste der Linkziele auf dieser Seite](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Hier finden Sie die Teilressourcen, die dieser Seite zugeordnet sind.](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Anzeigen des Seiteninhalts

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMPage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) ab, die den Seiteninhalt enthält. Wenn die Seite nicht in die XPS OM geladen wurde, wie dies geschieht, wenn das XPS OM durch Aufrufen von [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile)initialisiert wird, wird die Seite durch Aufrufen von [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) in das XPS OM geladen.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Abrufen der Liste der Linkziele auf dieser Seite

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMNameCollection-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) ab, die die Liste der Seitenelemente enthält, die Linkziele sind. Wenn die Seite nicht in das XPS OM geladen wurde, wird die Liste der Linkziele aus dem **PageContent.LinkTargets-Markup** gelesen. Wenn die Seite geladen wurde, überprüft [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) jedes Element auf der Seite und gibt eine Liste von Elementen zurück, deren **IsHyperlinkTarget-Attribut** **TRUE ist.**


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Hier finden Sie die Teilressourcen, die dieser Seite zugeordnet sind.

Das folgende Codebeispiel ruft die Listen der verschiedenen Ressourcen ab, die von dieser Seite verwendet werden.


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

[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




