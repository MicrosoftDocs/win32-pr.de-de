---
title: Abrufen und Festlegen einer Abkürzungs Taste
description: In diesem Thema wird veranschaulicht, wie Sie die Tastenkombination für ein Hot Key-Steuerelement abrufen oder festlegen.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106340545"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="d2026-103">Abrufen und Festlegen einer Abkürzungs Taste</span><span class="sxs-lookup"><span data-stu-id="d2026-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="d2026-104">In diesem Thema wird veranschaulicht, wie Sie die Tastenkombination für ein Hot Key-Steuerelement abrufen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="d2026-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="d2026-105">Die [**HKM \_ SetHotKey**](hkm-sethotkey.md) -Nachricht ermöglicht einer Anwendung die Festlegung der Tastenkombination für ein Hot Key-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d2026-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="d2026-106">Anwendungen verwenden die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um den Code des virtuellen Schlüssels und die Modifiziererflags des vom Benutzer ausgewählten Hot Key abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2026-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d2026-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d2026-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d2026-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="d2026-108">Technologies</span></span>

-   [<span data-ttu-id="d2026-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d2026-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d2026-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d2026-110">Prerequisites</span></span>

-   <span data-ttu-id="d2026-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2026-111">C/C++</span></span>
-   <span data-ttu-id="d2026-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d2026-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d2026-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d2026-113">Instructions</span></span>


<span data-ttu-id="d2026-114">Verwenden Sie die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um den Code des virtuellen Schlüssels und die modifiziererschlüssel abzurufen, die einen vom Benutzer ausgewählten Kürzungs Schlüssel beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2026-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="d2026-115">Verwenden Sie die [**HKM \_ SetHotKey**](hkm-sethotkey.md) -Nachricht, um diese Werte für einen Hot Key festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d2026-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="d2026-116">Im folgenden C++-Codebeispiel verwendet die Anwendungs definierte Funktion die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um eine Tastenkombination aus einem Abkürzungs Schlüssel-Steuerelement abzurufen, und verwendet dann die [**WM \_ SetHotKey**](/windows/desktop/inputdev/wm-sethotkey) -Nachricht, um eine globale Hot Key-Nachricht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d2026-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="d2026-117">Beachten Sie, dass Sie keine globale Taste für ein Fenster mit dem untergeordneten Fenster Stil von [**WS \_**](/windows/desktop/winmsg/window-styles) festlegen können.</span><span class="sxs-lookup"><span data-stu-id="d2026-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2026-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2026-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2026-119">Referenz zur Hot Key-Steuerung</span><span class="sxs-lookup"><span data-stu-id="d2026-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d2026-120">Informationen zu Hot Key-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d2026-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="d2026-121">Verwenden von Hot Key-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d2026-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 