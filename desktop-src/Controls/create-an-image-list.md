---
title: Erstellen einer Bildliste
description: In diesem Thema wird veranschaulicht, wie mit der ImageList- \_ Funktion Create eine Bildliste erstellt wird.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949241"
---
# <a name="how-to-create-an-image-list"></a><span data-ttu-id="a9d53-103">Erstellen einer Bildliste</span><span class="sxs-lookup"><span data-stu-id="a9d53-103">How to Create an Image List</span></span>

<span data-ttu-id="a9d53-104">In diesem Thema wird veranschaulicht, wie mit der [**ImageList-Funktion \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) eine Bildliste erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9d53-104">This topic demonstrates how to use the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function to create an image list.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a9d53-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a9d53-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a9d53-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="a9d53-106">Technologies</span></span>

-   [<span data-ttu-id="a9d53-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a9d53-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a9d53-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a9d53-108">Prerequisites</span></span>

-   <span data-ttu-id="a9d53-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a9d53-109">C/C++</span></span>
-   <span data-ttu-id="a9d53-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="a9d53-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a9d53-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a9d53-111">Instructions</span></span>


<span data-ttu-id="a9d53-112">Sie erstellen eine Bildliste, indem Sie die Create-Funktion von [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a9d53-112">You create an image list by calling the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function.</span></span> <span data-ttu-id="a9d53-113">Zu den Parametern zählen der Typ der zu erstellenden Bildliste, die Dimensionen der einzelnen Bilder und die Anzahl der Bilder, die Sie der Liste hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="a9d53-113">The parameters include the type of image list to create, the dimensions of each image, and the number of images that you intend to add to the list.</span></span>

<span data-ttu-id="a9d53-114">Im folgenden Beispiel wird eine maskierte Bildliste erstellt, und das-Makro der [**ImageList- \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) wird verwendet, um der Liste zwei Symbole hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a9d53-114">The following example creates a masked image list and uses the [**ImageList\_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) macro to add two icons to the list.</span></span>



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="a9d53-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9d53-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d53-116">Referenz zu Bildlisten</span><span class="sxs-lookup"><span data-stu-id="a9d53-116">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="a9d53-117">Informationen zu Bildlisten</span><span class="sxs-lookup"><span data-stu-id="a9d53-117">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="a9d53-118">Verwenden von Bildlisten</span><span class="sxs-lookup"><span data-stu-id="a9d53-118">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




