---
description: Wenn ein Gerät erstellt wird, erstellt die Windows-Abbild Beschaffung (WIA) eine hierarchische Struktur von WIA-Elementen, die das Gerät und die diesem Gerät zugeordneten Ordner und Bilder darstellen.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Auflisten von Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216053"
---
# <a name="enumerating-items"></a><span data-ttu-id="262fc-103">Auflisten von Elementen</span><span class="sxs-lookup"><span data-stu-id="262fc-103">Enumerating Items</span></span>

<span data-ttu-id="262fc-104">Wenn ein Gerät erstellt wird, erstellt die Windows-Abbild Beschaffung (WIA) eine hierarchische Struktur von WIA-Elementen, die das Gerät und die diesem Gerät zugeordneten Ordner und Bilder darstellen.</span><span class="sxs-lookup"><span data-stu-id="262fc-104">When a device is created, Windows Image Acquisition (WIA) creates a hierarchical tree of WIA items that represent the device and the folders and images associated with that device.</span></span> <span data-ttu-id="262fc-105">Verwenden Sie das Stamm Element (das Element im Stamm der Struktur, das das Gerät darstellt) [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (oder [**IWiaItem2:: enumchilditems**](-wia-iwiaitem2-enumchilditems.md))-Methode, um ein Enumeratorobjekt zu erstellen und einen Zeiger auf seine [**ienumwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) -Schnittstelle (oder [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) zu erhalten, die zum Navigieren in der Elementstruktur und zum Abrufen des Zugriffs auf die dem Gerät zugeordneten Bilder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="262fc-105">Use the root item's (the item at the root of the tree that represents the device) [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method to create an enumerator object and obtain a pointer to its [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (or [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) interface, which is used to navigate the item tree and gain access to the images or scanning beds associated with the device.</span></span>

<span data-ttu-id="262fc-106">Das folgende Beispiel zeigt eine Funktion, die rekursiv alle Elemente einer Struktur auflistet, beginnend mit einem Stamm Element, das an die Funktion weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="262fc-106">The following example shows a function that recursively enumerates all of the items of a tree, beginning with a root item that is passed to the function.</span></span>


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



<span data-ttu-id="262fc-107">Die-Funktion übernimmt den-Parameter **pwiaitem**, einen Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle (oder [**IWiaItem2**](-wia-iwiaitem2.md)) des Stamm Elements der Elementstruktur zum auflisten.</span><span class="sxs-lookup"><span data-stu-id="262fc-107">The function takes the parameter **pWiaItem**, a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (or [**IWiaItem2**](-wia-iwiaitem2.md)) interface of the root item of the item tree to enumerate.</span></span>

<span data-ttu-id="262fc-108">Zuerst überprüft die Funktion, ob es sich bei dem Element um einen Ordner oder Anlagen handelt.</span><span class="sxs-lookup"><span data-stu-id="262fc-108">First, the function checks to see whether the item is a folder or if it has attachments.</span></span> <span data-ttu-id="262fc-109">Wenn dies der Fall ist, wird die [**iwiaitem:: enumchilditems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (oder [**IWiaItem2:: enumchilditems**](-wia-iwiaitem2-enumchilditems.md))-Methode von **pwiaitem** aufgerufen, um ein Enumeratorobjekt für die Elementstruktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="262fc-109">If it does, it then calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method of **pWiaItem** to create an enumerator object for the item tree.</span></span> <span data-ttu-id="262fc-110">Wenn dieser Aufruf erfolgreich ist und der Enumerator gültig ist, durchläuft die Funktion die untergeordneten Elemente und ruft rekursiv für jedes Element auf, wobei die einzelnen Elemente als potenzielles Stamm Element für die nächste Ebene untergeordneter Elemente behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="262fc-110">If this call succeeds, and the enumerator is valid, the function iterates through the child items, and recursively calls itself on each item, treating each as a potential root item for the next level of child items.</span></span>

<span data-ttu-id="262fc-111">Auf diese Weise listet die-Funktion alle Verzweigungen der Elementstruktur unterhalb des Stamm Elements auf, das an **EnumerateItems** weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="262fc-111">In this manner, the function enumerates all branches of the item tree below the root item passed to **EnumerateItems**.</span></span>

 

 



