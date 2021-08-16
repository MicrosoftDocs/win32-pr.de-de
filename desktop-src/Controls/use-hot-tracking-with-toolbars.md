---
title: Verwenden von Hot-Tracking mit Symbolleisten
description: Wenn ein Mauszeiger auf ein Element zeigt, wird das Element heiß. Wenn hot-tracking aktiviert ist, wird das heiße Element hervorgehoben. Eine Symbolleiste, die mit dem TBSTYLE \_ FLAT-Stil erstellt wird, oder eine Symbolleiste, die visuelle Stile verwendet, unterstützt standardmäßig hot-tracking.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd735828675ca360cfa91aceefb2d76d34252a96aa7b5edb776e3d48a1fcdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829085"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Verwenden von Hot-Tracking mit Symbolleisten

Wenn ein Mauszeiger auf ein Element zeigt, wird das Element heiß. Wenn hot-tracking aktiviert ist, wird das heiße Element hervorgehoben. Eine Symbolleiste, die mit dem [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) erstellt wird, oder eine Symbolleiste, die [visuelle Stile](themes-overview.md)verwendet, unterstützt standardmäßig hot-tracking.

Für die Heiße Nachverfolgung müssen Sie Imagelisten erstellen. Aus diesem Grund können Sie die [**\_ TB-ADDBITMAP-Nachricht**](tb-addbitmap.md) oder die [**CreateToolbarEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) nicht verwenden, um ihre Symbolleiste zu erstellen.

Wenn der Mauszeiger auf eine Symbolleistenschaltfläche zeigt, wird die Schaltfläche umranden, um sie hervorzuheben. Die folgende Abbildung zeigt eine Symbolleiste mit aktivierter Hot-Tracking- der Mauszeiger auf die Schaltfläche Speichern gezeigt hat, als der Screenshot aufgenommen wurde.

![Screenshot eines Dialogfelds mit einer Drei-Elemente-Symbolleiste das ausgewählte Symbol wird umranden.](images/tb-withstyles.png)

Wenn sie möchten, dass sich eine Bitmap der Symbolleistenschaltfläche ändert, wenn sich der Zustand des Steuerelements ändert, speichern Sie die verschiedenen Bilder in [Bildlisten.](image-lists.md) Einige Anwendungen verfügen z. B. über schwarze und weiße Symbolleistenschaltflächen, die farbig werden, wenn sie ausgewählt werden. Die beiden verschiedenen Bilder werden in Bildlisten gespeichert. Symbolleisten unterstützen die Verwendung von bis zu drei Bildlisten. In der Regel verfügt eine Anwendung über eine Standardmäßige, deaktivierte und hot-tracking-Liste von Bildern. Verwenden Sie die TB [**\_ SETHOTIMAGELIST- und TB GETHOTIMAGELIST-Meldungen,**](tb-sethotimagelist.md) um Bildlisten für hot-Symbolleistenschaltflächen festzulegen und abzurufen. [**\_**](tb-gethotimagelist.md)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-hot-tracking-with-a-toolbar"></a>Verwenden von Hot-Tracking mit einer Symbolleiste

Im folgenden Codebeispiel wird eine Bildliste für hot-Schaltflächen erstellt, ausgefüllt und zugewiesen.


```C++
// Create the image list, himlHot.
g_himlHot = ImageList_Create(MYICON_CX,MYICON_CY,ILC_COLOR8,0,4);

// Load a bitmap from a resource file, and add the images to the image list.
// Note that the bitmap contains four images.

hBitmapHot = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_HOT));

ImageList_Add(g_himlHot, hBitmapHot, NULL);
   
// Set the image list. 
SendMessage(hwndTB, TB_SETHOTIMAGELIST, 0, (LPARAM)g_himlHot);
   
// Loop to fill the array of TBBUTTON structures.  
for(i=0;i<MAX_BUTTONS;i++)
{
    tbArray[i].iBitmap   = i;                   // Bitmap from image list.
    tbArray[i].idCommand = IDM_BUTTONSTART + i;
    tbArray[i].fsState   = TBSTATE_ENABLED;
    tbArray[i].fsStyle   = BTNS_DROPDOWN;
    tbArray[i].dwData    = 0;
    tbArray[i].iString   = i;
}

DeleteObject(hBitmapHot);    // Delete the loaded bitmap.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleistensteuerelementen](using-toolbar-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




