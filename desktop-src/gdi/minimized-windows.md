---
description: Das System reduziert das Hauptfenster einer Anwendung (Überlappendes Format) in ein minimiertes Fenster, wenn der Benutzer im Menü "Fenster" auf "minimieren" klickt, oder die Anwendung die Funktion "ShowWindow" aufruft und einen Wert wie z \_ . b. SW
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Minimierte Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754377"
---
# <a name="minimized-windows"></a><span data-ttu-id="b5217-103">Minimierte Fenster</span><span class="sxs-lookup"><span data-stu-id="b5217-103">Minimized Windows</span></span>

<span data-ttu-id="b5217-104">Das System reduziert das Hauptfenster einer Anwendung (Überlappendes Format) in ein minimiertes Fenster, wenn der Benutzer im Menü "Fenster" auf "minimieren" klickt, oder die Anwendung die Funktion " [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) " aufruft und einen Wert wie z \_ . b. SW</span><span class="sxs-lookup"><span data-stu-id="b5217-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="b5217-105">Durch das Minimieren eines Fensters wird die Systemleistung beschleunigt, indem die Arbeitsschritte reduziert werden, die eine Anwendung beim Aktualisieren des Hauptfensters ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="b5217-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="b5217-106">Bei einer typischen Anwendung zeichnet das System ein Symbol, das als Klassen Symbol bezeichnet wird, wenn das Fenster minimiert wird, wobei das Symbol mit dem Namen des Fensters beschriftet wird.</span><span class="sxs-lookup"><span data-stu-id="b5217-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="b5217-107">Das Klassen Symbol, ein statisches Bild, das die Anwendung darstellt, wird von der Anwendung beim Registrieren der Fenster Klasse angegeben.</span><span class="sxs-lookup"><span data-stu-id="b5217-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="b5217-108">Die Anwendung weist dem Klassen Symbol dem **HICON** -Member von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ein Handle zu, bevor [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5217-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="b5217-109">Die Anwendung kann die [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion verwenden, um das Symbol Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b5217-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
