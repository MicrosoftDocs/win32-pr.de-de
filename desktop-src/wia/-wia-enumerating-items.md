---
description: Wenn ein Gerät erstellt wird, erstellt Windows Image Acquisition (WIA) eine hierarchische Struktur von WIA-Elementen, die das Gerät und die diesem Gerät zugeordneten Ordner und Bilder darstellen.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Aufzählen von Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438e5cb65b701fcbc24d61aa888ac6c88347cacdaca8fa0a861f8c452a1ebc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772880"
---
# <a name="enumerating-items"></a>Aufzählen von Elementen

Wenn ein Gerät erstellt wird, erstellt Windows Image Acquisition (WIA) eine hierarchische Struktur von WIA-Elementen, die das Gerät und die diesem Gerät zugeordneten Ordner und Bilder darstellen. Verwenden Sie die [**IWiaItem::EnumChildItems(oder**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) [**IWiaItem2::EnumChildItems)-Methode**](-wia-iwiaitem2-enumchilditems.md)des Stammelements (das Element im Stamm der Struktur, das das Gerät darstellt), um ein Enumeratorobjekt zu erstellen und einen Zeiger auf die [**IEnumWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (oder [**IEnumWiaItem2)**](-wia-ienumwiaitem2.md)zu erhalten. , die verwendet wird, um durch die Elementstruktur zu navigieren und Zugriff auf die Bilder oder Scanbilder zu erhalten, die dem Gerät zugeordnet sind.

Das folgende Beispiel zeigt eine Funktion, die rekursiv alle Elemente einer Struktur aufzählt, beginnend mit einem Stammelement, das an die Funktion übergeben wird.


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



Die Funktion verwendet den **Parameter pWiaItem,** einen Zeiger auf die [**IWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (oder [**IWiaItem2)**](-wia-iwiaitem2.md)des Stammelements der Elementstruktur, das aufzählt werden soll.

Zunächst überprüft die Funktion, ob es sich bei dem Element um einen Ordner handelt oder ob es über Anlagen verfügt. In diesem Beispiel wird die [**IWiaItem::EnumChildItems-Methode**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (oder [**IWiaItem2::EnumChildItems)**](-wia-iwiaitem2-enumchilditems.md)von **pWiaItem** zum Erstellen eines Enumeratorobjekts für die Elementstruktur aufruft. Wenn dieser Aufruf erfolgreich ist und der Enumerator gültig ist, durchfingt die Funktion die untergeordneten Elemente und ruft sich rekursiv für jedes Element auf und behandelt jedes element als potenzielles Stammelement für die nächste Ebene untergeordneter Elemente.

Auf diese Weise listet die Funktion alle Verzweigungen der Elementstruktur unterhalb des Stammelements auf, das an **EnumerateItems übergeben wird.**

 

 



