---
description: Wenn mehrere Monitore als unabhängige anzeigen verwendet werden, enthält der Desktop einen Bildschirm oder eine Reihe von anzeigen.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Verwenden mehrerer Monitore als unabhängige Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980505"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="8d486-103">Verwenden mehrerer Monitore als unabhängige Anzeige</span><span class="sxs-lookup"><span data-stu-id="8d486-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="8d486-104">Wenn mehrere Monitore als unabhängige anzeigen verwendet werden, enthält der Desktop einen Bildschirm oder eine Reihe von anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d486-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="8d486-105">Diese Gruppe von Anzeigen enthält immer den primären Monitor und verhält sich wie in den anderen Abschnitten dieses Themas beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d486-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="8d486-106">Eine Anwendung kann jeden anderen Monitor als unabhängige Anzeige verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d486-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="8d486-107">Die Verwendung anderer Monitore als unabhängige anzeigen wird für Treiber, die für das Windows-Anzeigetreiber Modell (WDDM) implementiert sind, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d486-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="8d486-108">Der Fenster-Manager weiß nichts über die unabhängigen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d486-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="8d486-109">Sie werden vollständig von der Anwendung gesteuert, und für die Anwendung sind keine Fenster-Manager-Funktionen verfügbar (alle Fenster-Manager-Aufrufe werden automatisch zur primären Anzeige geleitet).</span><span class="sxs-lookup"><span data-stu-id="8d486-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="8d486-110">Jede unabhängige Anzeige verfügt über eigene Ursprungs-und horizontale und vertikale Koordinaten, und der Zugriff erfolgt über die GDI-Funktionen wie z. b. " [**kreatedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) " oder die DirectX-Funktionen wie " **directdrawcreate**".</span><span class="sxs-lookup"><span data-stu-id="8d486-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="8d486-111">Zum Auffinden der unabhängigen Anzeige aufrufen Sie " [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) " und suchen nach den anzeigen, für die das Flag "Gerät anzeigen" \_ \_ \_ \_ in der [**Anzeige \_ Geräte**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) Struktur nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d486-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="8d486-112">Eine Anwendung kann eine Anzeige öffnen, indem Sie aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8d486-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="8d486-113">In diesem Befehl ist der *lpszdisplayname* -Parameter einer der von [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) zurückgegebenen Gerätenamen, und *lpdevmode* ist eine Beschreibung des Grafikmodus für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="8d486-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="8d486-114">Der resultierende HDC kann verwendet werden, um einen beliebigen Grafik Vorgang für das Gerät auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d486-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



