---
title: Vorgehensweise beim Hinzufügen eines Elements zu einem Header Steuerelement
description: In diesem Thema wird veranschaulicht, wie ein Element einem Header-Steuerelement hinzugefügt wird.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949243"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="fd21a-103">Vorgehensweise beim Hinzufügen eines Elements zu einem Header Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fd21a-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="fd21a-104">In diesem Thema wird veranschaulicht, wie ein Element einem Header-Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fd21a-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="fd21a-105">Ein Header Steuerelement verfügt in der Regel über mehrere Header Elemente, die die Spalten des Steuer Elements definieren.</span><span class="sxs-lookup"><span data-stu-id="fd21a-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="fd21a-106">Sie können einem Header-Steuerelement ein Element hinzufügen, indem Sie die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht an das-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="fd21a-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fd21a-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="fd21a-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fd21a-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="fd21a-108">Technologies</span></span>

-   [<span data-ttu-id="fd21a-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fd21a-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fd21a-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fd21a-110">Prerequisites</span></span>

-   <span data-ttu-id="fd21a-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="fd21a-111">C/C++</span></span>
-   <span data-ttu-id="fd21a-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="fd21a-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fd21a-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="fd21a-113">Instructions</span></span>


<span data-ttu-id="fd21a-114">Verwenden Sie die [**HDM \_ InsertItem**](hdm-insertitem.md) -Nachricht, um dem Header Steuerelement ein Element hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd21a-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="fd21a-115">Die Nachricht muss die Adresse einer [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="fd21a-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="fd21a-116">Diese Struktur definiert die Eigenschaften des Header Elements, das eine Zeichenfolge, ein Bitmap-Bild, eine Anfangs Größe und einen Anwendungs definierten 32-Bit-Wert enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="fd21a-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="fd21a-117">Im folgenden Beispiel wird veranschaulicht, wie die [**HDM- \_ InsertItem**](hdm-insertitem.md) -Nachricht und die [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur verwendet werden, um ein Element zu einem Header-Steuerelement hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd21a-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="fd21a-118">Das neue Element besteht aus einer Zeichenfolge, die innerhalb des Element Rechtecks linksbündig ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="fd21a-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="fd21a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd21a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd21a-120">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fd21a-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="fd21a-121">Header Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="fd21a-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="fd21a-122">Verwenden von Header Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fd21a-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




