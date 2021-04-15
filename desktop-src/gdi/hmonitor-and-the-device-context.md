---
description: Jede physische Anzeige wird durch ein Monitor Handle des Typs Hmonitor dargestellt.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: Hmonitor und der Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993982"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="16f20-103">Hmonitor und der Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="16f20-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="16f20-104">Jede physische Anzeige wird durch ein Monitor Handle des Typs **Hmonitor** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="16f20-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="16f20-105">Ein gültiger **Hmonitor** ist garantiert ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="16f20-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="16f20-106">Eine physische Anzeige hat denselben **Hmonitor** , solange Sie Teil des Desktops ist.</span><span class="sxs-lookup"><span data-stu-id="16f20-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="16f20-107">Wenn eine " **WM \_ displaychange** "-Meldung gesendet wird, kann jeder Monitor vom Desktop entfernt werden, sodass der zugehörige **Hmonitor** ungültig wird oder seine Einstellungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="16f20-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="16f20-108">Daher sollte eine Anwendung überprüfen, ob alle **hmonitors** gültig sind, wenn diese Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="16f20-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="16f20-109">Jede Funktion, die einen Anzeigegeräte Kontext (DC) zurückgibt, gibt normalerweise einen Domänen Controller für den primären Monitor zurück.</span><span class="sxs-lookup"><span data-stu-id="16f20-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="16f20-110">Verwenden Sie die Funktion " [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) ", um den DC für einen anderen Monitor zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16f20-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="16f20-111">Oder Sie können den Gerätenamen aus der [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) -Funktion verwenden, um einen Domänen Controller mit " [**kreatedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="16f20-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="16f20-112">Wenn die Funktion, wie z. b. [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), jedoch einen Domänen Controller für ein Fenster erhält, das mehr als eine Anzeige umfasst, wird der Domänen Controller auch die beiden anzeigen überspannen.</span><span class="sxs-lookup"><span data-stu-id="16f20-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



