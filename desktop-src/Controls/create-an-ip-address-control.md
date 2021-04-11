---
title: Erstellen eines IP-Adress Steuer Elements
description: In diesem Thema wird veranschaulicht, wie eine Instanz eines IP-Adress Steuer Elements erstellt wird.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102570"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="0833a-103">Erstellen eines IP-Adress Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="0833a-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="0833a-104">In diesem Thema wird veranschaulicht, wie eine Instanz eines IP-Adress Steuer Elements erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0833a-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0833a-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="0833a-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0833a-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="0833a-106">Technologies</span></span>

-   [<span data-ttu-id="0833a-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="0833a-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0833a-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0833a-108">Prerequisites</span></span>

-   <span data-ttu-id="0833a-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0833a-109">C/C++</span></span>
-   <span data-ttu-id="0833a-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="0833a-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0833a-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0833a-111">Instructions</span></span>


<span data-ttu-id="0833a-112">Vor dem Erstellen eines IP-Adress Steuer Elements können Sie die DLL für allgemeine Steuerelemente durch Aufrufen von [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)laden.</span><span class="sxs-lookup"><span data-stu-id="0833a-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="0833a-113">Verwenden Sie dann die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", um eine Instanz-IP-Adress Steuerung zu erstellen</span><span class="sxs-lookup"><span data-stu-id="0833a-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="0833a-114">Der Klassenname für das-Steuerelement ist [**WC- \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="0833a-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="0833a-115">Verwenden Sie den untergeordneten [**WS \_**](/windows/desktop/winmsg/window-styles) -Stil, da dem IP-Adress Steuerelement keine bestimmte Stil Konstante zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0833a-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="0833a-116">Im folgenden C++-Codebeispiel ruft die Anwendungs definierte Funktion zuerst [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) auf und legt den **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur auf die " [**ICC \_ Internet \_ Classes**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)"-Klasse fest, die die IP-Adress Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="0833a-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="0833a-117">Anschließend wird " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, um eine Instanz des Steuer Elements für die IP-Adresse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0833a-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="0833a-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0833a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0833a-119">IP-Adress Steuerungs Verweis</span><span class="sxs-lookup"><span data-stu-id="0833a-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0833a-120">Informationen zu IP-Adress Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0833a-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="0833a-121">Verwenden von IP-Adress Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0833a-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 