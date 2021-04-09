---
title: Verwenden von Hot-Tracking mit Symbolleisten
description: Wenn ein Mauszeiger über ein Element bewegt wird, wird das Element in den heiß. Wenn die Hot-Tracking-Funktion aktiviert ist, wird das heiße Element hervorgehoben. Eine Symbolleiste, die mit dem flachen Stil tbstyle erstellt wird \_ , oder eine Symbolleiste, die visuelle Stile verwendet, unterstützt standardmäßig Hot-Tracking.
ms.assetid: E77B15D7-F0C9-41F7-8BE9-30260FA4BB0C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a486407b8dafade1e3bba083c5a56f3a9be2adcf
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104038708"
---
# <a name="how-to-use-hot-tracking-with-toolbars"></a>Verwenden von Hot-Tracking mit Symbolleisten

Wenn ein Mauszeiger über ein Element bewegt wird, wird das Element in den heiß. Wenn die Hot-Tracking-Funktion aktiviert ist, wird das heiße Element hervorgehoben. Eine Symbolleiste, die mit dem [**\_ flachen Stil tbstyle**](toolbar-control-and-button-styles.md) erstellt wird, oder eine Symbolleiste, die [visuelle Stile](themes-overview.md)verwendet, unterstützt standardmäßig Hot-Tracking.

Die Hot-Tracking erfordert, dass Sie Bildlisten erstellen; Daher können Sie Ihre Symbolleiste nicht mithilfe der [**TB- \_ AddBitmap**](tb-addbitmap.md) -Nachricht oder [**der Funktion "**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) -Funktion" in der Funktion "Anordnen" erstellen.

Wenn die Maus über eine Symbolleisten Schaltfläche bewegt wird, wird die Schaltfläche so dargestellt, dass Sie hervorgehoben wird In der folgenden Abbildung ist eine Symbolleiste mit aktivierter Hot-Tracking-Funktion dargestellt. der Mauszeiger befand sich auf die Schaltfläche "Speichern", als der Screenshot erstellt wurde.

![Screenshot eines Dialog Felds mit einer drei-Element-Symbolleiste das ausgewählte Symbol wird angezeigt.](images/tb-withstyles.png)

Wenn Sie möchten, dass sich die Bitmap einer Symbolleisten-Schaltfläche ändert, wenn sich der Zustand des Steuer Elements ändert, speichern Sie die verschiedenen Bilder in [Bildlisten](image-lists.md). Beispielsweise verfügen einige Anwendungen über schwarze und weiße Symbolleisten Schaltflächen, die bei der Auswahl angezeigt werden. Die beiden unterschiedlichen Bilder werden in Bildlisten gespeichert. Symbolleisten unterstützen die Verwendung von bis zu drei Bildlisten. In der Regel verfügt eine Anwendung über eine standardmäßige, deaktivierte und nach Verfolgungs Liste von Bildern. Um Bildlisten für heiße Symbolleisten Schaltflächen festzulegen und abzurufen, verwenden Sie die TB-Meldungen [**\_ SetHotImageList**](tb-sethotimagelist.md) und [**TB \_ gethotimagelist**](tb-gethotimagelist.md) .

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-hot-tracking-with-a-toolbar"></a>Verwenden von Hot-Tracking mit einer Symbolleiste

Im folgenden Codebeispiel wird eine Bildliste für Hot Buttons erstellt, ausgefüllt und zugewiesen.


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

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




