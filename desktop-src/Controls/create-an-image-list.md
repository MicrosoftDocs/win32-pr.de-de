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
# <a name="how-to-create-an-image-list"></a>Erstellen einer Bildliste

In diesem Thema wird veranschaulicht, wie mit der [**ImageList-Funktion \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) eine Bildliste erstellt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Sie erstellen eine Bildliste, indem Sie die Create-Funktion von [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) aufrufen. Zu den Parametern zählen der Typ der zu erstellenden Bildliste, die Dimensionen der einzelnen Bilder und die Anzahl der Bilder, die Sie der Liste hinzufügen möchten.

Im folgenden Beispiel wird eine maskierte Bildliste erstellt, und das-Makro der [**ImageList- \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) wird verwendet, um der Liste zwei Symbole hinzuzufügen.



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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Bildlisten](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informationen zu Bildlisten](image-lists.md)
</dt> <dt>

[Verwenden von Bildlisten](using-image-lists.md)
</dt> </dl>

 

 




