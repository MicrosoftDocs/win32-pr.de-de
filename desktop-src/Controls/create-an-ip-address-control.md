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
# <a name="how-to-create-an-ip-address-control"></a>Erstellen eines IP-Adress Steuer Elements

In diesem Thema wird veranschaulicht, wie eine Instanz eines IP-Adress Steuer Elements erstellt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Vor dem Erstellen eines IP-Adress Steuer Elements können Sie die DLL für allgemeine Steuerelemente durch Aufrufen von [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)laden. Verwenden Sie dann die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", um eine Instanz-IP-Adress Steuerung zu erstellen Der Klassenname für das-Steuerelement ist [**WC- \_ IPAddress**](common-control-window-classes.md). Verwenden Sie den untergeordneten [**WS \_**](/windows/desktop/winmsg/window-styles) -Stil, da dem IP-Adress Steuerelement keine bestimmte Stil Konstante zugeordnet ist.

Im folgenden C++-Codebeispiel ruft die Anwendungs definierte Funktion zuerst [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) auf und legt den **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur auf die " [**ICC \_ Internet \_ Classes**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)"-Klasse fest, die die IP-Adress Klasse angibt. Anschließend wird " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " aufgerufen, um eine Instanz des Steuer Elements für die IP-Adresse zu erstellen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IP-Adress Steuerungs Verweis](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[Informationen zu IP-Adress Steuerelementen](ip-address-controls.md)
</dt> <dt>

[Verwenden von IP-Adress Steuerelementen](using-ip-address-controls.md)
</dt> </dl>

 

 