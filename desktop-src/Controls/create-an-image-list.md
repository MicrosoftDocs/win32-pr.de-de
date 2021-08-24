---
title: Erstellen einer Bildliste
description: In diesem Thema wird veranschaulicht, wie Sie die ImageList \_ Create-Funktion verwenden, um eine Bildliste zu erstellen.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04e3e22894546e887e1a4ca5348518b4e4a35c45f4a26b5b6125b81f9323bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826480"
---
# <a name="how-to-create-an-image-list"></a>Erstellen einer Bildliste

In diesem Thema wird veranschaulicht, wie Sie die [**ImageList \_ Create-Funktion verwenden,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) um eine Bildliste zu erstellen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Sie erstellen eine Bildliste, indem Sie die [**ImageList \_ Create-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) aufrufen. Die Parameter umfassen den Typ der zu erstellenden Bildliste, die Dimensionen der einzelnen Bilder und die Anzahl der Bilder, die Sie der Liste hinzufügen möchten.

Im folgenden Beispiel wird eine maskierte Bildliste erstellt und das [**Makro ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) verwendet, um der Liste zwei Symbole hinzuzufügen.



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

 

 




