---
title: Vorgehensweise beim Verwenden von Virtual List-View-Steuerelementen
description: In diesem Thema wird veranschaulicht, wie Sie mit virtuellen Listenansicht-Steuerelementen arbeiten.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "106363064"
---
# <a name="how-to-use-virtual-list-view-controls"></a><span data-ttu-id="d4a92-103">Vorgehensweise beim Verwenden von Virtual List-View-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d4a92-103">How to Use Virtual List-View Controls</span></span>

<span data-ttu-id="d4a92-104">In diesem Thema wird veranschaulicht, wie Sie mit virtuellen Listenansicht-Steuerelementen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4a92-104">This topic demonstrates how to work with virtual list-view controls.</span></span> <span data-ttu-id="d4a92-105">In den begleitenden C++-Codebeispielen wird veranschaulicht, wie Sie die Benachrichtigungs Meldungen des virtuellen Listen-Ansichts Steuer Elements verarbeiten, den Cache optimieren und ein Element aus dem Cache abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4a92-105">The accompanying C++ code examples show how to process virtual list-view control notification messages, how to optimize the cache, and how to retrieve an item from the cache.</span></span>

-   [<span data-ttu-id="d4a92-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d4a92-106">What you need to know</span></span>](#what-you-need-to-know)
-   [<span data-ttu-id="d4a92-107">Benachrichtigungs Codes für die virtuelle List-View Steuerung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d4a92-107">Process Virtual List-View Control Notification Codes</span></span>](#process-virtual-list-view-control-notification-codes)
-   [<span data-ttu-id="d4a92-108">Optimieren des Caches</span><span class="sxs-lookup"><span data-stu-id="d4a92-108">Optimize the Cache</span></span>](#optimize-the-cache)
-   [<span data-ttu-id="d4a92-109">Abrufen eines Elements aus dem Cache</span><span class="sxs-lookup"><span data-stu-id="d4a92-109">Retrieve an Item From the Cache</span></span>](#retrieve-an-item-from-the-cache)
-   [<span data-ttu-id="d4a92-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4a92-110">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="d4a92-111">Der Beispielcode in diesem Abschnitt setzt voraus, dass der Cache ein dynamisch zugewiesenes Array von Anwendungs definierten Strukturen ist.</span><span class="sxs-lookup"><span data-stu-id="d4a92-111">The example code in this section assumes that the cache is a dynamically allocated array of application-defined structures.</span></span> <span data-ttu-id="d4a92-112">Die Struktur wird im folgenden C++-Codebeispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="d4a92-112">The structure is defined in the following C++ code example.</span></span>

 


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



## <a name="what-you-need-to-know"></a><span data-ttu-id="d4a92-113">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d4a92-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d4a92-114">Technologien</span><span class="sxs-lookup"><span data-stu-id="d4a92-114">Technologies</span></span>

-   [<span data-ttu-id="d4a92-115">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d4a92-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d4a92-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d4a92-116">Prerequisites</span></span>

-   <span data-ttu-id="d4a92-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="d4a92-117">C/C++</span></span>
-   <span data-ttu-id="d4a92-118">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d4a92-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d4a92-119">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d4a92-119">Instructions</span></span>

### <a name="process-virtual-list-view-control-notification-codes"></a><span data-ttu-id="d4a92-120">Benachrichtigungs Codes für die virtuelle List-View Steuerung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d4a92-120">Process Virtual List-View Control Notification Codes</span></span>

<span data-ttu-id="d4a92-121">Zusätzlich zu den von anderen Listenansicht-Steuerelementen gesendeten Benachrichtigungs Codes können auch virtuelle Listenansicht-Steuerelemente die [LVN- \_ odcachehint](lvn-odcachehint.md) -und LVN-Benachrichtigungs Codes von [**\_ odfinditem**](lvn-odfinditem.md) senden.</span><span class="sxs-lookup"><span data-stu-id="d4a92-121">In addition to the notification codes sent by other list-view controls, virtual list-view controls can also send the [LVN\_ODCACHEHINT](lvn-odcachehint.md) and [**LVN\_ODFINDITEM**](lvn-odfinditem.md) notification codes.</span></span>

<span data-ttu-id="d4a92-122">Diese Anwendungs definierte Funktion verarbeitet Benachrichtigungs Meldungen, die häufig von einem Virtual List-View-Steuerelement gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4a92-122">This application-defined function handles notification messages that are commonly sent from a virtual list-view control.</span></span>


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



### <a name="optimize-the-cache"></a><span data-ttu-id="d4a92-123">Optimieren des Caches</span><span class="sxs-lookup"><span data-stu-id="d4a92-123">Optimize the Cache</span></span>

<span data-ttu-id="d4a92-124">Ein virtuelles Listenansicht-Steuerelement sendet eine [LVN- \_ odcachehint](lvn-odcachehint.md) -Benachrichtigungs Meldung, wenn sich der Inhalt seines Anzeige Bereichs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d4a92-124">A virtual list-view control sends a [LVN\_ODCACHEHINT](lvn-odcachehint.md) notification message when the contents of its display area have changed.</span></span> <span data-ttu-id="d4a92-125">Die Meldung enthält Informationen über den Bereich von Elementen, die zwischengespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4a92-125">The message contains information about the range of items to be cached.</span></span> <span data-ttu-id="d4a92-126">Nachdem Sie die Benachrichtigungs Meldung erhalten haben, muss Ihre Anwendung darauf vorbereitet sein, den Cache mit Element Informationen für den angeforderten Bereich zu laden, damit die Informationen sofort verfügbar sind, wenn eine [LVN \_ getdispinfo](lvn-getdispinfo.md) -Benachrichtigungs Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a92-126">Upon receiving the notification message, your application must be prepared to load the cache with item information for the requested range so that the information will be readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification message is sent.</span></span>

<span data-ttu-id="d4a92-127">Im folgenden C++-Codebeispiel nimmt die Anwendungs definierte Funktion den Bereich der Elemente für den Cache an, der von einem virtuellen Listenansicht-Steuerelement gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a92-127">In the following C++ code example, the application-defined function accepts the range of items for the cache that is sent by a virtual list-view control.</span></span> <span data-ttu-id="d4a92-128">Es wird eine Überprüfung durchgeführt, um zu bestimmen, dass der angeforderte Bereich von Elementen nicht bereits zwischengespeichert ist, und dann wird der erforderliche globale Speicher zugewiesen und ggf. der Cache ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d4a92-128">It performs a verification to determine that the requested range of items is not already cached, and then it allocates the required global memory and fills the cache if necessary.</span></span>


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



### <a name="retrieve-an-item-from-the-cache"></a><span data-ttu-id="d4a92-129">Abrufen eines Elements aus dem Cache</span><span class="sxs-lookup"><span data-stu-id="d4a92-129">Retrieve an Item From the Cache</span></span>

<span data-ttu-id="d4a92-130">Diese Beispiel Funktion akzeptiert zwei Parameter: die Adresse der Anwendungs definierten Struktur und einen ganzzahligen Wert, der den Index des Elements in der Liste darstellt.</span><span class="sxs-lookup"><span data-stu-id="d4a92-130">This example function accepts two parameters, the address of the application-defined structure and an integer value representing the index of the item in the list.</span></span> <span data-ttu-id="d4a92-131">Der Indexwert wird überprüft, um zu ermitteln, ob das gewünschte Element zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d4a92-131">It checks the index value to discover if the desired item is cached.</span></span> <span data-ttu-id="d4a92-132">Wenn dies der Fall ist, wird der Zeiger, der an die Funktion übermittelt wurde, auf einen Speicherort im Cache festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4a92-132">If it is, the pointer that was passed to the function is set to a location in the cache.</span></span> <span data-ttu-id="d4a92-133">Wenn sich das Element nicht im Haupt-oder endcache befindet, müssen die Element Informationen manuell gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d4a92-133">If the item is not in the main or end cache, the item information must be located manually.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="d4a92-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4a92-134">Remarks</span></span>

<span data-ttu-id="d4a92-135">Eine Liste der Fenster Meldungen, die von einem Listenansicht-Steuerelement verarbeitet werden, finden Sie unter [Standard List-View Nachrichtenverarbeitung](listview-message-processing.md).</span><span class="sxs-lookup"><span data-stu-id="d4a92-135">For a list of the window messages processed by a list-view control, see [Default List-View Message Processing](listview-message-processing.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="d4a92-136">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4a92-136">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4a92-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4a92-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a92-138">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="d4a92-138">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d4a92-139">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d4a92-139">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="d4a92-140">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d4a92-140">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




