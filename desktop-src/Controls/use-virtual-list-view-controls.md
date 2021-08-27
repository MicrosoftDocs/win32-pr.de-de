---
title: Verwenden von Virtual List-View-Steuerelementen
description: In diesem Thema wird das Arbeiten mit virtuellen Listenansichtssteuerelementen veranschaulicht.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6ed847d7cb8a41e4cb1c255290ff660eb278bcd99126605a2874c52b279e694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059700"
---
# <a name="how-to-use-virtual-list-view-controls"></a>Verwenden von Virtual List-View-Steuerelementen

In diesem Thema wird das Arbeiten mit virtuellen Listenansichtssteuerelementen veranschaulicht. Die zugehörigen C++-Codebeispiele zeigen, wie Benachrichtigungsmeldungen zu virtuellen Listenansichtssteuerelements, wie der Cache optimiert wird und wie ein Element aus dem Cache abgerufen wird.

-   [Wichtige Informationen](#what-you-need-to-know)
-   [Verarbeiten von Benachrichtigungscodes List-View virtuellen Steuerelementen](#process-virtual-list-view-control-notification-codes)
-   [Optimieren des Caches](#optimize-the-cache)
-   [Abrufen eines Elements aus dem Cache](#retrieve-an-item-from-the-cache)
-   [Zugehörige Themen](#related-topics)

> [!Note]  
> Im Beispielcode in diesem Abschnitt wird davon ausgegangen, dass der Cache ein dynamisch zugeordnetes Array von anwendungsdefinierten Strukturen ist. Die -Struktur wird im folgenden C++-Codebeispiel definiert.

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="process-virtual-list-view-control-notification-codes"></a>Verarbeiten von Benachrichtigungscodes List-View virtuellen Steuerelementen

Zusätzlich zu den Benachrichtigungscodes, die von anderen Listenansichtssteuerelementen gesendet werden, können virtuelle Listenansichtssteuerelemente auch die [LVN \_ ODCACHEHINT-](lvn-odcachehint.md) und [**LVN \_ ODFINDITEM-Benachrichtigungscodes**](lvn-odfinditem.md) senden.

Diese anwendungsdefinierte Funktion verarbeitet Benachrichtigungsmeldungen, die häufig von einem virtuellen Listenansicht-Steuerelement gesendet werden.


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a>Optimieren des Caches

Ein virtuelles Listenansicht-Steuerelement sendet eine [LVN \_ ODCACHEHINT-Benachrichtigungsmeldung,](lvn-odcachehint.md) wenn sich der Inhalt des Anzeigebereichs geändert hat. Die Meldung enthält Informationen über den Bereich von Elementen, die zwischengespeichert werden sollen. Beim Empfang der Benachrichtigungsmeldung muss Ihre Anwendung darauf vorbereitet sein, den Cache mit Elementinformationen für den angeforderten Bereich zu laden, damit die Informationen sofort verfügbar sind, wenn eine [LVN \_ GETDISPINFO-Benachrichtigungsmeldung](lvn-getdispinfo.md) gesendet wird.

Im folgenden C++-Codebeispiel akzeptiert die anwendungsdefinierte Funktion den Bereich von Elementen für den Cache, der von einem virtuellen Listenansicht-Steuerelement gesendet wird. Er führt eine Überprüfung durch, um zu ermitteln, ob der angeforderte Bereich von Elementen noch nicht zwischengespeichert ist. Anschließend wird der erforderliche globale Arbeitsspeicher reserviert und der Cache bei Bedarf auffüllt.


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a>Abrufen eines Elements aus dem Cache

Diese Beispielfunktion akzeptiert zwei Parameter, die Adresse der anwendungsdefinierten Struktur und einen ganzzahligen Wert, der den Index des Elements in der Liste darstellt. Der Indexwert wird überprüft, um zu prüfen, ob das gewünschte Element zwischengespeichert wird. Wenn dies der Ansicht ist, wird der Zeiger, der an die Funktion übergeben wurde, auf einen Speicherort im Cache festgelegt. Wenn sich das Element nicht im Haupt- oder Endcache befindet, müssen die Elementinformationen manuell gespeichert werden.


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a>Hinweise

Eine Liste der Fenstermeldungen, die von einem Listenansicht-Steuerelement verarbeitet werden, finden Sie unter [List-View Message Processing](listview-message-processing.md).

## <a name="complete-example"></a>Vollständiges Beispiel

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[List-View-Steuerelementreferenz](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




